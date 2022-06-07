# HBase

HBase es una columna de base de datos orientada al construido en la parte superior de la Hadoop sistema de archivos. Es un proyecto de código abierto y se puede escalar horizontalmente.

HBase es un modelo de datos que es similar a Google la gran tabla diseñada para permitir el rápido acceso aleatorio a enormes cantidades de datos estructurados. Aprovecha la tolerancia a errores de sistema de archivos el Hadoop (HDFS).

Uno puede almacenar los datos de los HDFS, bien directamente o a través HBase. Consumidor de datos lee y tiene acceso a los datos en forma aleatoria usando HBase HDFS. HBase se sitúa en la parte superior de la Hadoop y Sistema de Archivos proporciona acceso de lectura y escritura.

![HDFS HBASE](..\img\hbase_flow.jpg)

## Mecanismo de almacenamiento en HBase

HBase es una **columna de base de datos** y las tablas en que se ordenan por fila. Esquema de la tabla define solamente la columna las familias, que son los pares de valor clave. Una tabla con varias columnas y cada columna familias familia puede tener cualquier número de columnas. Los valores de columna se almacenan fisicamente en el disco. Cada valor de la celda de la tabla tiene una marca de tiempo. En resumen, en un HBase:

- Tabla es un conjunto de filas.
- Fila es una colección de la columna.
- Columna familia es una colección de columnas.
- Columna es una recopilación de los principales pares de valores.

## Características de HBase

- HBase es lineal escalable.
- Ha hecho automático.
- Proporciona lectura coherente y escrituras.
- Se integra con Hadoop, tanto como un origen y un destino.
- Tiene fácil API de java para el cliente.
- Proporciona replicación de datos en clústeres.
