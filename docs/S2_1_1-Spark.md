# Spark Core 

Apache Spark es un framework de procesamiento distribuido para Big Data. La característica principal es el uso que hace de las estructuras de datos en memoria llamadas RDD, con lo que consigue aumentar el rendimiento frente a herramientas como Hadoop considerablemente.

- **Procesamiento en memoria**: Apache Spark es 100 veces más rápido en memoria y 10 veces más rápido en disco que Hadoop MapReduce, para ello necesita más recursos.
- **Soporta múltiples lenguajes**: Spark tiene APIs disponibles en los lenguajes Java, Scala, Python y R.
- **Analítica avanzada**: Para ello, soporta consultas SQL y su uso para Machine Learning con librerías de data science como MLlib y GraphX.
- **Abstracción RDD** (Resilient Distributed Dataset): consiste en una colección inmutable de elementos en memoria distribuída.
- **Evaluación perezosa**: Las transformaciones sobre los datos solo se resuelven al ejecutar una acción sobre ellos.

  ![Ecosistema y componentes de Apache Spark](https://aprenderbigdata.com/wp-content/uploads/ecosistema-apache-spark.png.webp)

## RDD

Resillent Distributed Datasets, se define como una colección de elementos que es tolerante a fallos y que es capaz de operar en paralelo. Este es el tipo principal de Spark, usa la evaluacion perezosa, se distrubuye por varias maquinas

