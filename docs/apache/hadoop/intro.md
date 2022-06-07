# Hadoop

Apache Hadoop es un entorno de trabajo para software, bajo licencia libre, para programar aplicaciones distribuidas que manejen grandes volúmenes de datos. Permite a las aplicaciones trabajar con miles de nodos en red y petabytes de datos.

## Hadoop core: HDFS

HDFS es el sistema de ficheros distribuido de Hadoop. El calificativo «distribuido» expresa la característica más significativa de este sistema de ficheros, la cual es su capacidad para almacenar los archivos en un clúster de varias máquinas.

> HDFS => Hadoop Distributed File System

### Arquitectura HDFS

![Basic HFFS architecture, with NameNode and multiple DataNodes.](https://phoenixnap.com/kb/wp-content/uploads/2021/04/hdfs-components-namenode-datanode-datanode.png)

Vamos a descomponer la arquitectura de **HDFS** en 3 componentes principales: NameNode, DataNode y Secondary NameNode.

#### NameNode

- Maestro
- Mantiene y maneja los nodo de datos
- Graba metadatos, es decir, información sobre los bloques de datos por ejemplo la localización de donde están, su tamaño...
- Recibe pulsaciones y reportes de todos los DataNodes

#### DataNodes

- Esclavo, contiene los demonios
- Guarda los datos
- Sirve para leer y escribir las peticiones de los clientes

> También el Secondary NameNode puede encontrarse como StandBy NameNode.
>
> [Parodia Secondary NameNode](https://www.youtube.com/watch?v=hEqQMLSXQlY)

#### Secondary NameNode

- Asume la responsabilidad del checkpoint por lo tanto, hace mas disponible el NameNode
- **Checkpoint: ** es el proceso de combinar editlogs con los FsImage (Por defecto, cada 1 hora)
- **EditsLogs: **registra cada cambio que ocurre en los metadatos del sistema de archivos
- **FsImage: **espacio de nombre de imagen que contiene la estructura completa del HDFS
- Habilita la conmutación por error mas rapida, asi previene de devolver los editslogs demasiado grandes.
- Si el NameNode cae, este asume el rol mientras el otro se recupera, pero nunca lo remplaza

### Funcionalidad de HDFS

**HDFS** se divide en bloques de 128mb excepto si de un archivo sobra un bloque que tenga menos, este ocupara lo que ocupe el sobrante por ejemplo 72mb. Se replica por defecto 3 veces entre los diferentes NameNodes pero esta configuración la puedes cambiar manualmente.

#### Proceso escritura

![Read And Write Operation In HDFS](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/read-and-write-operation-in-hdfs/Images/image001.jpg)

El cliente informa al NameNode que quiere escribir, este hace sus comprobaciones y le devuelve una lista de DataNodes donde puede hacerlo, el cliente escribe en ellos, se hacen las replicas y escriben, una vez teerminado le envían al cliente un informe indicando si ha salido correcto. El NameNode recibe este mensaje de vuelta y si es correcto actualiza el metadato.

#### Proceso lectura

![HDFS Architecture](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/read-and-write-operation-in-hdfs/Images/image006.jpg)

El cliente le envia la ruta del archivo que quiere leer al NameNode y este le devuelve informacion del archivo, principalmente donde se contiene y se la devuelve al cliente. El cliente encuentra el DataNode correspondiente y obtiene los bloques uno a uno, luego agrega y combina localmente los bloques para obtener el archivo completo.

## Hadoop Core:  MapReduce

Es un framework que habita la distribución y el paralelismo en procesado de grandes conjuntos de datos. Tiene dos fases principales **Map** y **Reduce**, por ello su nombre.

![Qué es Hadoop MapReduce? Introducción - Aprender BIG DATA](https://aprenderbigdata.com/wp-content/uploads/MapReduce-esquema-1024x615.png)

- **Fase Map:** se ejecuta en subtareas llamada mappers. Responsable de generar clave-valor, filtrando, agrupando, ordenando o transformando datos originales.
- **Fase Shuffle: ** puede que no sea siempre necesaria, es un paso medio entre el map y reduce, que ayuda a recoger los datos y ordenarlos de manera conveniente para su procesamiento.
- **Fase Reduce: **gestiona la agregación de los valores devolviendo un resultado final.



## Hadoop Core:  YARN

Es la capa de administración de recursos del clúster para el ecosistema hadoop, que se encarga de escribir trabajos y asignar recursos. Permite a hadoop soportar varios motores de ejecución como mapreduce y proporciona un planificador agnóstico a los trabajos.

![El ecosistema Hadoop: hacia una pila tecnológica Apache para Big Data |  Blog de Mikel Niño: Industria 4.0, Big Data Analytics, emprendimiento  digital, modelos de negocio](http://2.bp.blogspot.com/-oTfrg8T0Q9w/VT5SKvNDSfI/AAAAAAAAFH0/bxwXqDfrpiA/s1600/apache-hadoop-ecosystem-by-thebigdatablog.png)

### Componentes de YARN

Tiene 3 componentes principales, en ellos están: Resource Manager, Node Manager y App Master

![Qué es Hadoop Yarn? Introducción - Aprender BIG DATA desde cero](https://aprenderbigdata.com/wp-content/uploads/arquitectura-hadoop-yarn.gif)

#### Resource Manager

 Se divide en dos subcomponentes, Scheduler y App Manager.

- **Scheduler: **gestiona la distribución de recursos del cluster, las aplicaciones usan los recursos que el Resource Manager les ha proporcionado. No monitoriza el estado de ninguna app, ni garantiza la ejecución .
- **App Manager: **responsable de aceptar peticiones de trabajo, negociar con el contenedor que la va a ejecutar y proporciona reinicio en caso de error.

#### Node Manager

Proporciona los recursos computacionales necesarios para las aplicaciones en forma de contenedores. Monitoriza la asignación de recursos (CPU, Red, Memoria y Disco)

#### App Master

Negocia los recursos apropiados con el Resource Manager y monitoriza su estado y progreso. Coordina la ejecución de todas las tareas de su app.
