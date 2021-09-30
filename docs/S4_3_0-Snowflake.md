# Snowflake

## Puntos clave que diferencia a Snowflake

En primer lugar es que es la única plataforma de datos **completamente** en la nube, también es totalmente escalable por el motivo que esta diseñada solo para la nube por lo que a su vez hereda todo el poder de la nube **(escalabilidad, elasticidad y almacenamiento ilimitado)**.

Snowflake tiene una arquitectura única y por capas desacopladas entre si, así como muchas características únicas como el tiempo viajado, 0% de clonado de datos, datos compartidos entre tantas.

Por ultimo a destacar tenemos que tiene muy pocos gastos generales de gestión mientras trabajamos con este

## Arquitectura

Contiene tres capas diferentes:

- capa de servicio
- capa de computación
- capa de almacenamiento
- ![Snowflake Cloud Data Warehouse 101: A Comprehensive Guide](https://lh5.googleusercontent.com/L5JnqaSeUBBDRabZwcOiwI08auyK19U8tCAfCuDWNmeg1FJlkHQvAIlC7uGZL0QYtZ_yP2krpXR-S9I-95y9ayFsxqXDgVhcNetWF5KbX00QnzY37smn_CO8xqhRUh5ATgBVRaKQ)

### Capa de almacenamiento

Es la capa que guarda todos los datos, veamos sus características: 

- Totalmente independiente de la computación. 
- Capacidad de almacenamiento de datos ilimitados (Virtualmente)
- Se divide en dos partes, física y lógica.
- Divide todos los datos en micro-particiones de 16mb cada una.
- Se replica 3 veces los archivos
- El formato de archivo es propio de Snowflake
- Los archivos son inmutables
- La definición de la tabla es lógica y se almacena en su capa de metadatos.

### Capa de computación [  Warehouse  ]

- Es la única forma de acceder a la capa de datos
- Escalabilidad horizontal y vertical
  - Puedes cambiar el tamaño de tu warehouse en ejecución y añadir mas nodos
- El tamaño varia entre X-small que tiene 1 cluster a 4X-Large con 128
- Todos los warehouse funcionan independientemente y su rendimiento no afecta a otras warehouses
- Todas las warehouses tienen su pequeño almacenamiento, que lo usa como cache para los datos de las queries, teniendo así un mejor rendimiento
- Se auto suspende cuando están parados

### Capa de servicio

Esta capa es el cerebro de snowflake porque toma el control de todos los componentes claves que permite que snowflake funcione mas rápido eficiente y efectivo.

se compone de los siguientes componentes: 

- Autenticación y control de acceso
- Administración de infraestructura
- Optimizador
- Administrador de metadatos
- Seguridad

Para conectarnos a el lo podremos hacer via ***consola*** o bien por cualquier driver **odbc / jdbc**. Siempre que estemos lanzando cualquier consulta para cualquier dato, esta detendrá esos datos, de forma que si otro usuario quiere hacer otra vez la misma query no tiene porque pasar por la capa de computación para procesar los datos.

Durante la carga de datos trackea que dato se encuentra en que partición. Otra cosa importante es que mantiene la consistencia de la transición entre Warehouse

## ¿Porque solo disponible en la nube?

- Ofrece una capacidad ilimitada y 3 copias por defecto de los datos
- Warehouse aprovecha el almacenamiento SSD para actuar como una cache
- Hereda la elasticidad, escalabilidad y la alta disponibilidad
- Tiene una gran pool de instancias lo que la hace mas rápido de escalar