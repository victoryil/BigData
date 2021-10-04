# Impala



Tecnologia de DB escalable y paralela sobre Hadoop, permitiendo realizar consultas sobre datos en HDFS o HBASE.

Ficheros: Lzo, sequenceTitle, Avro, RcFile y parquet. Auth rol basado en Sentry, driver ODBC y SQL de Hive.

El servidor de impala es un motor de DB distribuido y de procesamiento paralelo masivo. Consiste en un conjunto de Demonios que corren sobre unos servidores dentro del clúster CDH.

![Impala - Architecture](https://www.tutorialspoint.com/impala/images/impala_architecture.jpg)

## Demonio

Uno de los componentes del core de impala es un demonio que corre en cada DataNode del clúster, físicamente representado por *impalad*. Lee y escribe los archivos de datos, acepta consultas y distribuye el trabajo sobre el clúster, transmite de vuelta los resultados de las consultas intermedias al nodo coordinador. Se puede enviar una consulta a cualquier demonio, es decir cualquier DataNode, y ese sera el nodo coordinador para esa consulta. Los otros nodos le envía los resultados parciales al coordinador y este lo construye. Cuando conectas la imapla shell, siempre conectas con el mismo DataNode por conveniencia. Si vas a explorar y repartiras la carga entre varios DataNodes cuando este en produccion.

Los demonios de Impala están en constante comunicación con StateStore para verificar que los nodos se encuentren en estado correcto y puedan aceptar nuevos trabajos. También reciben mensajes desde el demonio Catalogd (Hive). Cuando algunos de los nodos de impala crea, modifica o elimina cualquier tipo de objeto, o inserción de datos, el Impala Demons transmite todas las acciones al resto de nodos. Esta comunicacion de fondo permite minimizar la necesidad de **Refresh** e **Invalidate Metadata** que veremos algo mas adelante.

## StateStore

Este verifica que los demonio están corriendo en todos los nodos y retransmiten continuamente sus estados a cada uno de ellos. Se representa en el proceso StateStore y solo se necesita un server por clúster. Si el demonio de Impala queda fuera por error de Hardware, red o cualquier cosa, StateStore informa a los otros demonios  para que en los futuras consultas se evite preguntar al nodo que este caído.

Como el propósito de StateStore es ayudar cuando algo va mal, no es un punto critico para el funcionamiento de un clúster de impala. Si el StateStore no esta corriendo o no es alcanzable los demonios continúan corriendo y distribuyendo el trabajo con normalidad. El clúster es menos robusto si otros demonios fallan mientras el StateStore esta fuera, cuando se recupera se restablece las comunicaciones.

## Catalog Service

Retransmite los cambios en los metadatos se hacen con las sentencias SQL de todos los DataNodes del clúster. Esta representados como catalogd, solo es necesario un demonio en un servidor del clúster. Como las peticiones son enviadas al StateStore, es recomendable que los dos demonios estén corriendo en la misma maquina. Este servicio evita tener que refrescar o invalidar los metadatos. Cuando se producen cambios a través de Hive o HDFS, los datos deben ser refrescado.

> Falta pasar la información sobre refresh y invalidate de impala y particionamiento dinamico, bucketing y agrupación de hive