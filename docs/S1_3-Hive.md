# Hive

es una infraestructura de almacenamiento de datos construida sobre Hadoop para proporcionar agrupación, consulta, y análisis de datos.

Hay 4 componentes principales en Hive:

* **Hadoop Core Component**
  
  * *HDFS*: cuando hive carga las tablas, internamente la guarda en una carpeta de HDFS y las rows en ficheros de texto
  * *MapReduce:* cuando ejecuta la consulta, se ejecuta el job de mapreduce correspondiente, convirtiendo o compilando la consulta en una clase Java. Nosotros lo construimos en el Jar y lo ejecutamos.
  
* **Metastore:** es el namespace de las tablas almacenadas en hive, contiene toda la informacion de hive, como los detalles relacionados con las tablas, columnas, particiones y localizacion en el almacenamiento

* **Drivers:** consultas del usuarios después de que el driver reciba la interfaz estando dentro. El driver implementa unn concepto de manejador de sesion, ejecuta y obtiene API´S. Modelado en la interfaz  JDBC/ ODBC que es proporcionado por el usuario, a su vez se divide en 4; Parser, Planner, Exectuion y Optimizer.

* **Cliente:** esta es la interfaz de la cual se entiva las consultas en Hive.

  ![Hive Architecture in Depth. Apache Hive is an ETL and Data… | by Jayvardhan  Reddy | Plumbers Of Data Science | Medium](https://miro.medium.com/max/628/0*d5DOvZIR_O4PPYlb)

### Job Execution Flows

1. Recibe una Query
2. Analiza HiveQL, realizando optimizacion de rendimiento
3. Planifica la ejecucion de la consulta
4. Toma la consulta y envia el trabajo al cluster
5. Monitoriza y procesa los datos en MapReduce o Apache Spark
6. Los datos se guardan en el HDFS.

### Hive Metastore

Es el componente que almacena el catalogo de sistemas que contiene los metadatos, que hemos comentado anteriormente. Hive usa DerbyDB una DB de java como MySQL que puede usarse para crear metastore.

### Curiosidades y datos de Hive

Hive ofreece varias interfaces para correr las consultas, como Hue o Beeline. 

Hue tiene una Ui a diferencia de beeline que es una linea de comandos.

Hive usa metastore como servicio de metadatos como comenteamos anteriormente, pues profundicemos mas. Una tabla en Hive es simplemente un directorio que contiene 0-N archivos. Su ruta predeterminada es: /user/hive/warehouse/tablename. Las tablas soportan muchos formatos de datos para guardar y recuperar informacion.