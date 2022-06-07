# Kafka

Kafka está diseñado para sistemas distribuidos de alto rendimiento. Kafka tiende a funcionar muy bien como reemplazo de un intermediario de mensajes más tradicional. En comparación con otros sistemas de mensajería, Kafka tiene un mejor rendimiento, partición integrada, replicación y tolerancia a fallas inherente, lo que lo hace ideal para aplicaciones de procesamiento de mensajes a gran escala.

## ¿Qué es Kafka?

Apache Kafka es un sistema de mensajería de publicación y suscripción distribuido y una cola robusta que puede manejar un gran volumen de datos y le permite pasar mensajes de un punto final a otro. Kafka es adecuado para el consumo de mensajes en línea y fuera de línea. Los mensajes de Kafka se conservan en el disco y se replican dentro del clúster para evitar la pérdida de datos. Kafka se basa en el servicio de sincronización de ZooKeeper. Se integra muy bien con Apache Storm y Spark para el análisis de datos de transmisión en tiempo real.

### Beneficios

Los siguientes son algunos beneficios de Kafka:

- **Confiabilidad** : Kafka es distribuido, particionado, replicado y tolerante a fallas.
- **Escalabilidad** : el sistema de mensajería de Kafka se escala fácilmente sin tiempo de inactividad.
- **Durabilidad** : Kafka utiliza un registro de confirmación distribuido , lo que significa que los mensajes persisten en el disco lo más rápido posible, por lo que es duradero.
- **Rendimiento** : Kafka tiene un alto rendimiento tanto para la publicación como para la suscripción de mensajes. Mantiene un rendimiento estable aunque se almacenen muchos TB de mensajes.

Kafka es muy rápido y garantiza cero tiempo de inactividad y cero pérdida de datos.

### Casos de uso

Kafka se puede utilizar en muchos casos de uso. Algunos de ellos se enumeran a continuación:

- **Métricas** : Kafka se usa a menudo para datos de monitoreo operativo. Esto implica agregar estadísticas de aplicaciones distribuidas para producir fuentes centralizadas de datos operativos.
- **Solución de agregación de registros** : Kafka se puede usar en una organización para recopilar registros de múltiples servicios y ponerlos a disposición en un formato estándar para múltiples consumidores.
- **Procesamiento** de transmisión: marcos populares como Storm y Spark Streaming leen datos de un tema, los procesan y escriben datos procesados en un nuevo tema donde están disponibles para usuarios y aplicaciones. La gran durabilidad de Kafka también es muy útil en el contexto del procesamiento de secuencias.







## ¿Qué es un sistema de mensajería?

Un Sistema de Mensajería es responsable de transferir datos de una aplicación a otra, por lo que las aplicaciones pueden enfocarse en los datos, pero no preocuparse por cómo compartirlos. La mensajería distribuida se basa en el concepto de colas de mensajes fiables. Los mensajes se ponen en cola de forma asíncrona entre las aplicaciones cliente y el sistema de mensajería. Hay dos tipos de patrones de mensajería disponibles: uno es punto a punto y el otro es un sistema de mensajería de publicación-suscripción (pub-sub). La mayoría de los patrones de mensajería siguen **pub-sub** .

### Sistema de mensajería punto a punto

En un sistema punto a punto, los mensajes se conservan en una cola. Uno o más consumidores pueden consumir los mensajes en la cola, pero un mensaje en particular puede ser consumido por un máximo de un solo consumidor. Una vez que un consumidor lee un mensaje en la cola, desaparece de esa cola. El ejemplo típico de este sistema es un Sistema de Procesamiento de Pedidos, donde cada pedido será procesado por un Procesador de Pedidos, pero varios Procesadores de Pedidos también pueden funcionar al mismo tiempo. El siguiente diagrama muestra la estructura.

![](..\img\point_to_point_messaging_system.jpg)

### Sistema de mensajería de publicación y suscripción

En el sistema de publicación-suscripción, los mensajes se conservan en un tema. A diferencia del sistema punto a punto, los consumidores pueden suscribirse a uno o más temas y consumir todos los mensajes de ese tema. En el sistema de publicación-suscripción, los productores de mensajes se denominan editores y los consumidores de mensajes se denominan suscriptores. Un ejemplo de la vida real es Dish TV, que publica diferentes canales como deportes, películas, música, etc., y cualquiera puede suscribirse a su propio conjunto de canales y obtenerlos siempre que los canales suscritos estén disponibles.

![](..\img\publish_subscribe_messaging_system.jpg)
