# Azure modulo 1

## Introducción

Azure es una plataforma de informática en la nube con un conjunto de servicios que se amplía continuamente para ayudarle a crear soluciones que satisfagan los objetivos empresariales. 

## ¿Por qué suele ser más barato usar la informática en la nube? 

Modelo de precios de pago por uso. Normalmente solo se paga por los servicios en la nube que se usan, lo que permite:

- Reducir los costos operativos.
- Ejecutar la infraestructura de forma más eficaz.
- Escalar a medida que cambien las necesidades empresariales.

## ¿Por qué debería migrar a la nube?

La nube ayuda a moverse con más rapidez, los equipos proporcionan nuevas características a los usuarios a velocidades récord. La nube proporciona acceso a petición para:

- Un grupo casi ilimitado de componentes de proceso, almacenamiento y redes sin procesar.
- Reconocimiento de voz y otros servicios cognitivos que ayudan a hacer que su aplicación destaque entre la multitud.
- Servicios de análisis que proporcionan datos de telemetría desde el software y los dispositivos.

## ¿Qué es Azure?

Es un conjunto de servicios en la nube, donde puedes hacer todas las gestiones desde el **portal de** **Azure**, donde podrás crear, configurar y controlar todos los recursos y servicios desde una sencilla y única Web App

## ¿Qué ofrece Azure?

- Innovación continua
- Mantiene un compromiso con el código abierto y admite todos los lenguajes y marcos, puede compilar como quiera e implementar donde quiera.
- Entorno híbrido
- Seguridad respaldada por un equipo de expertos.

## ¿Cómo funciona Azure?

Azure es una plataforma en cloud privada y publica que ayuda a los desarrolladores y los administradores de IT a construir, desplegar y administrar sus aplicaciones. Azure usa la virtualización separando entre un acoplamiento ajustado entre el hardware y el sistema operativo usando una capa de abstracción llamada ***hypervisor***.

El hypervisor emula todas las funciones de un ordenador real y su CPU en una maquina virtual, optimiza la capacidad de la obstrucción por hardware. Este puede correr múltiples maquinas virtuales a la vez y cada una puede correr cualquier sistema operativo compatible.

Microsoft tiene centros de datos por todo el mundo, cada centro de datos tiene racks lleno de servidores y cada servidor incluye **Hypervisor** para correr las multiples maquinas virtuales, un Switch de red que provee la conectividad para todos los servidores. Se ejecuta un servidor en cada rack con un software especial llamado **Frabric Controller**.

Cada Fabric Controller esta conectado a otra pieza especial de software conocida como **Orchestator**, este es el responsable de administrar todo lo que pasa en Azure, incluyendo las peticiones del usuario. El usuario hace las peticiones usando la web API de Orchestator, la cual puede ser llamada por varias herramientas incluida la interfaz de Azure Portal.

Cuando un usuario hace una peticion para crear una maquina virtual, Orchestator empaqueta todo lo necesario, elige el mejor servidor rack, y manda esos paquetes y peticion al Fabric Controller. Una vez que el Fabric Controller crea la maquina, el usuario puede conectar con ella.

## ¿Qué es Azure Portal? 

Es una consola unificada basada en web que proporciona una alternativa a las herramientas de línea de comandos. Con Azure Portal, puede administrar la suscripción de Azure mediante una interfaz gráfica de usuario. Puede:

- Compile, administre y supervise todo, desde aplicaciones web sencillas hasta complejas implementaciones en la nube.
- Cree paneles personalizados para una vista organizada de recursos.
- Configure opciones de accesibilidad para una experiencia óptima.

![Captura de pantalla en la que se muestra Azure Portal.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/intro-to-azure-fundamentals/media/azure-portal-dd184579.png)

## ¿Qué es Azure Marketplace?

Facilita la conexión entre los usuarios y los partners de Microsoft, proveedores de software independientes y nuevas empresas que ofrecen sus soluciones y servicios, optimizados para ejecutarse en Azure. Los clientes de Azure Marketplace pueden buscar, probar, comprar y aprovisionar aplicaciones y servicios de cientos de los principales proveedores de servicios. Todas las soluciones y los servicios están certificados para ejecutarse en Azure.

![Captura de pantalla en la que se muestra Azure Marketplace.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/intro-to-azure-fundamentals/media/marketplace-6ca0b9bb.png)

## Servicios de Azure

![Diagrama en el que se muestra la vista general de los servicios de Azure populares con secciones para seguridad y administración, servicios de plataforma, nube híbrida y servicios de infraestructura.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/intro-to-azure-fundamentals/media/azure-services-6c41a736.png)

### Proceso

Azure proporciona una amplia gama de opciones para hospedar aplicaciones y servicios.

|       Nombre del servicio        |                     Función del servicio                     |
| :------------------------------: | :----------------------------------------------------------: |
|      Azure Virtual Machines      | Máquinas virtuales (VM) Windows o Linux hospedadas en Azure. |
| Azure Virtual Machine Scale Sets | Escalado de máquinas virtuales Windows o Linux hospedadas en Azure. |
|     Azure Kubernetes Service     | Administración de clústeres para máquinas virtuales que ejecutan servicios en contenedores. |
|       Azure Service Fabric       | Plataforma de sistemas distribuidos que se ejecuta en Azure o en el entorno local. |
|           Azure Batch            | Servicio administrado para aplicaciones informáticas de alto rendimiento y paralelas. |
|    Azure Container Instances     | Aplicaciones en contenedores que se ejecutan en Azure sin necesidad de aprovisionar servidores ni máquinas virtuales. |
|         Azure Functions          | Un servicio de procesos sin servidor y controlado por eventos |

### Redes

La vinculación de recursos de proceso y el suministro de acceso a las aplicaciones es la función clave de la red de Azure.

|    **Nombre del servicio**     |                   **Función del servicio**                   |
| :----------------------------: | :----------------------------------------------------------: |
|     Azure Virtual Network      | Conecta máquinas virtuales a conexiones de red privada virtual (VPN) entrantes. |
|      Azure Load Balancer       | Equilibra las conexiones entrantes y salientes a aplicaciones o puntos de conexión de servicio. |
|   Azure Application Gateway    | Optimiza la entrega de granjas de servidores de aplicaciones y, al mismo tiempo, aumenta la seguridad de las aplicaciones. |
|       Azure VPN Gateway        | Accede a redes de Azure Virtual Network mediante puertas de enlace de VPN de alto rendimiento. |
|           Azure DNS            | Proporciona respuestas DNS ultrarrápidas y disponibilidad de dominio extremadamente alta. |
| Azure Content Delivery Network | Entrega contenido de gran ancho de banda a los clientes globalmente. |
|     Azure DDoS Protection      | Protege las aplicaciones hospedadas en Azure frente a ataques por denegación de servicio distribuido (DDoS). |
|     Azure Traffic Manager      | Distribuye el tráfico de red entre las regiones de Azure en todo el mundo. |
|       Azure ExpressRoute       | Se conecta a Azure mediante conexiones seguras de gran ancho de banda dedicadas. |
|     Azure Network Watcher      | Supervisa y diagnostica problemas de red mediante el análisis basado en el escenario. |
|         Azure Firewall         | Implementa un firewall de alta seguridad y alta disponibilidad con escalabilidad ilimitada. |
|       Azure Virtual WAN        | Crea una red de área extensa (WAN) unificada que conecta sitios locales y remotos. |

### Almacenamiento

Azure proporciona cuatro tipos principales de servicios de almacenamiento.

| **Nombre del servicio** |                   **Función del servicio**                   |
| :---------------------: | :----------------------------------------------------------: |
|   Azure Blob Storage    | Servicio de almacenamiento para objetos muy grandes, como archivos de vídeo o mapas de bits. |
|   Azure File storage    | Recursos compartidos de archivos que puede administrar como un servidor de archivos y acceder a ellos del mismo modo. |
|   Azure Queue Storage   | Almacén de datos para la puesta en cola y la entrega confiable de mensajes entre aplicaciones. |
|   Azure Table storage   | Table Storage es un servicio que almacena datos estructurados no relacionales (también conocidos como datos NoSQL estructurados) en la nube, lo que proporciona un almacén de claves y atributos con un diseño sin esquema. |

Todos estos servicios comparten varias características:

- **Durabilidad** y alta disponibilidad con redundancia y la replicación.
- **Seguridad** mediante el cifrado automático y control de acceso basado en rol.
- **Escalabilidad** con un almacenamiento prácticamente ilimitado.
- **Administración** y control del mantenimiento y de cualquier problema crítico que pueda surgir.
- **Accesibilidad** desde cualquier parte del mundo a través de HTTP o HTTPS.

### Móvil

Los desarrolladores pueden crear servicios de back-end móviles para aplicaciones iOS, Android y Windows de forma rápida y sencilla. 

Estas son las características de este servicio:

- Sincronización de datos sin conexión.
- Conectividad a datos locales.
- Difusión de notificaciones de inserción.
- Escalado automático para satisfacer las necesidades del negocio.

### Bases de datos

Azure proporciona varios servicios de base de datos para almacenar una gran variedad de volúmenes y tipos de datos. Y con la conectividad global, los usuarios disponen de estos datos al instante.

| **Nombre del servicio**              | **Función del servicio**                                     |
| ------------------------------------ | ------------------------------------------------------------ |
| Azure Cosmos DB                      | Base de datos distribuida globalmente que admite opciones NoSQL. |
| Azure SQL Database                   | Base de datos relacional totalmente administrada con escalado automático, inteligencia integral y seguridad sólida. |
| Azure Database for MySQL             | Base de datos relacional MySQL totalmente administrada y escalable con alta disponibilidad y seguridad. |
| Azure Database for PostgreSQL        | Base de datos relacional PostgreSQL totalmente administrada y escalable con alta disponibilidad y seguridad. |
| SQL Server en Azure Virtual Machines | Servicio que hospeda aplicaciones empresariales de SQL Server en la nube. |
| Azure Synapse Analytics              | Almacén de datos totalmente administrado con seguridad integral en todos los niveles de escala sin costo adicional. |
| Azure Database Migration Service     | Servicio que migra bases de datos a la nube sin cambios en el código de aplicación. |
| Azure Cache for Redis                | Servicio totalmente administrado que almacena en caché datos estáticos y usados con frecuencia para reducir la latencia de datos y aplicaciones. |
| Azure Database for MariaDB           | Base de datos relacional MariaDB totalmente administrada y escalable con alta disponibilidad y seguridad. |

### Web

Azure incluye soporte técnico de primera clase para compilar y hospedar aplicaciones web y servicios web basados en HTTP.

|           **Nombre del servicio**            |                       **Descripción**                        |
| :------------------------------------------: | :----------------------------------------------------------: |
|              Azure App Service               | Creación rápida de aplicaciones en la nube eficaces basadas en web. |
|           Azure Notification Hubs            | Envíe notificaciones push a cualquier plataforma desde cualquier back-end. |
|             Azure API Management             | Publique API para desarrolladores, asociados y empleados de forma segura y a escala. |
|            Azure Cognitive Search            | Esta búsqueda completamente administrada se implementa como servicio. |
| Característica Web Apps de Azure App Service | Cree e implemente rápidamente aplicaciones web críticas a escala. |
|            Servicio Azure SignalR            |  Agregue funcionalidades web en tiempo real con facilidad.   |

### IoT

| **Nombre del servicio** |                       **Descripción**                        |
| :---------------------: | :----------------------------------------------------------: |
|       IoT Central       | Solución global de software como servicio (SaaS) de IoT totalmente administrada que facilita la conexión, la supervisión y la administración de los recursos de IoT a escala. |
|      Azure IoT Hub      | Centro de mensajería que proporciona comunicaciones y supervisión seguras entre millones de dispositivos de IoT. |
|        IoT Edge         | Servicio totalmente administrado que permite insertar los modelos de análisis de datos directamente en los dispositivos IoT, lo que les permite responder rápidamente a los cambios de estado sin necesidad de consultar modelos de IA basados en la nube. |

### Macrodatos

Se han desarrollado tecnologías de clúster de código abierto para tratar con estos grandes conjuntos de datos. Azure admite una amplia gama de tecnologías y servicios para proporcionar soluciones de análisis y macrodatos.

### 

| **Nombre del servicio** |                       **Descripción**                        |
| :---------------------: | :----------------------------------------------------------: |
| Azure Synapse Analytics | Ejecute análisis a gran escala mediante un almacenamiento de datos empresarial basado en la nube que aprovecha las ventajas del procesamiento paralelo masivo para ejecutar rápidamente consultas complejas en petabytes de datos. |
|   HDInsight de Azure    | Procese grandes cantidades de datos con los clústeres administrados de Hadoop en la nube. |
|    Azure Databricks     | Integre este servicio de análisis colaborativo basado en Apache Spark con otros servicios de macrodatos en Azure. |

### Inteligencia  Artificial

En el contexto de la informática en la nube, la inteligencia artificial se basa en una amplia gama de servicios, donde el principal es el aprendizaje automático.

Estos son algunos de los tipos de servicios de inteligencia artificial y aprendizaje automático más comunes de Azure.

|    **Nombre del servicio**     |                       **Descripción**                        |
| :----------------------------: | :----------------------------------------------------------: |
| Azure Machine Learning Service | Entorno basado en la nube que puede usar para desarrollar, entrenar, probar, implementar, administrar y realizar un seguimiento de los modelos de aprendizaje automático. Puede generar y ajustar automáticamente un modelo. Le permite comenzar a entrenar en el equipo local y luego escalar horizontalmente a la nube. |
|        Azure ML Studio         | Área de trabajo visual colaborativa donde puede compilar, probar e implementar soluciones de aprendizaje automático mediante algoritmos de aprendizaje automático predefinidos y módulos de control de datos. |

*Cognitive Services* es un conjunto de productos estrechamente relacionados. Puede usar estas API precompiladas en las aplicaciones para solucionar problemas complejos.

|      **Nombre del servicio**      |                       **Descripción**                        |
| :-------------------------------: | :----------------------------------------------------------: |
|              Visión               | Use algoritmos de procesamiento de imágenes para identificar, subtitular, indexar y moderar imágenes y vídeos. |
|                Voz                | Convierta voz en texto, use la voz para la comprobación o agregue reconocimiento del hablante a la aplicación. |
|    Asignación de conocimiento     | Asigne información y datos complejos para resolver tareas como las de recomendaciones inteligentes y búsqueda semántica. |
|            Bing Search            | Agregue las Bing Search API a sus aplicaciones y aproveche la capacidad de combinar miles de millones de páginas web, imágenes, vídeos y noticias con una sola llamada API. |
| Procesamiento de lenguaje natural | permita que las aplicaciones procesen lenguaje natural con scripts precompilados, evalúen opiniones y aprendan a reconocer lo que quieren los usuarios. |

### DevOps

DevOps reúne a individuos, procesos y tecnología mediante la automatización de la entrega de software para ofrecer un valor continuo a los usuarios. Con Azure DevOps puede crear, *compilar* y *publicar* canalizaciones que proporcionan integración, entrega e implementación continuas a las aplicaciones. Puede integrar los repositorios y las pruebas de aplicaciones, realizar la supervisión de aplicaciones y trabajar con artefactos de compilación. También puede trabajar con elementos de trabajo pendiente para realizar el seguimiento, automatizar la implementación de la infraestructura e integrar una gama de herramientas y servicios de terceros como Jenkins y Chef. 

| **Nombre del servicio** |                       **Descripción**                        |
| :---------------------: | :----------------------------------------------------------: |
|      Azure DevOps       | Use herramientas de colaboración de desarrollo como canalizaciones de alto rendimiento, repositorios Git privados gratuitos, paneles Kanban configurables y completas pruebas de carga basadas en la nube y automatizadas. Anteriormente conocido como Visual Studio Team Services. |
|   Azure DevTest Labs    | Cree rápidamente entornos de Windows y Linux a petición para probar o realizar demostraciones de las aplicaciones directamente desde canalizaciones de implementación. |

## Introducción a las cuentas de Azure

Para crear y usar los servicios de Azure, necesita una suscripción de Azure.

![Ilustración en la que se muestran los diferentes niveles del ámbito de la cuenta.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/intro-to-azure-fundamentals/media/scope-levels-12669ee1.png)

Una vez vista la jerarquía vertical de la organización, describamos cada uno de estos niveles empezando desde abajo:

- **Recursos**: Los recursos son instancias de servicios que puede crear, como máquinas virtuales, almacenamiento o bases de datos SQL.
- **Grupos de recursos**: Los recursos se combinan en grupos de recursos, que actúan como contenedor lógico en el que se implementan y administran recursos de Azure como aplicaciones web, bases de datos y cuentas de almacenamiento.
- **Suscripciones**: Una suscripción agrupa las cuentas de usuario y los recursos que han creado esas cuentas de usuario. Para cada suscripción, hay límites o cuotas en la cantidad de recursos que se pueden crear y usar. Las organizaciones pueden usar las suscripciones para administrar los costos y los recursos creados por los usuarios, equipos o proyectos.
- **Grupos de administración**: Estos grupos le ayudan a administrar el acceso, las directivas y el cumplimiento de varias suscripciones. Todas las suscripciones de un grupo de administración heredan automáticamente las condiciones que se aplican al grupo de administración.

## Regiones de Azure

Una *región* es un área geográfica del planeta que contiene al menos un centro de datos, aunque podrían ser varios centros de datos cercanos y conectados mediante una red de baja latencia. Azure asigna y controla los recursos de forma inteligente dentro de cada región para garantizar que las cargas de trabajo están bien compensadas.

### ¿Por qué son importantes las regiones?

Estas regiones le dan la flexibilidad necesaria para acercar las aplicaciones a los usuarios estén donde estén. Las regiones globales proporcionan una mejor escalabilidad y redundancia, y conservan la residencia de datos para los servicios.

### Regiones de Azure especiales

Azure tiene regiones especializadas que se pueden usar al crear las aplicaciones, en lo referente al cumplimiento normativo o a aspectos legales.

- **US DoD (centro), US Gov Virginia, US Gov Iowa y más:** Estas regiones son instancias físicas y lógicas con aislamiento de red de Azure para asociados y agencias de la administración pública de EE. UU. Estos centros de datos están operados por personal estadounidense sometido a evaluación e incluyen certificaciones de cumplimiento adicionales.
- **Este de China, Norte de China y más:** Estas regiones están disponibles gracias a una asociación exclusiva entre Microsoft y 21Vianet, por la cual Microsoft no mantiene directamente los centros de datos.

## Zonas de disponibilidad de Azure

Las zonas de disponibilidad son centros de datos separados físicamente dentro de una región de Azure. Cada zona de disponibilidad consta de uno o varios centros de datos equipados con alimentación, refrigeración y redes independientes. Una zona de disponibilidad se configura para constituir un *límite de aislamiento*. Si una zona deja de funcionar, la otra continúa trabajando. Las zonas de disponibilidad están conectadas a través de redes de fibra óptica de alta velocidad privadas.

![Diagrama en el que se muestran tres centros de datos conectados dentro de una sola región de Azure que representa una zona de disponibilidad.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/availability-zones-5c3c490c.png)

> No todas las regiones son compatibles con las zonas de disponibilidad.

## Pares de regiones de Azure

Cada región de Azure se empareja siempre con otra región de la misma zona geográfica (por ejemplo, EE. UU., Europa o Asia) que se encuentre como mínimo a 500 km de distancia.

![Diagrama en el que se muestra la relación entre el par de regiones, la geografía, la región y el centro de datos.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/region-pairs-d9eb9728.png)

Ventajas adicionales de los pares de región:

- Si se produce una gran interrupción de Azure, se da prioridad a una región de cada par para asegurarse de que al menos una se restaure lo más rápido posible para las aplicaciones hospedadas en ese par de regiones.
- Las actualizaciones planeadas de Azure se implementan una a una en regiones emparejadas para minimizar el tiempo de inactividad y el riesgo de interrupción de la aplicación.
- Los datos siguen residiendo en la misma zona geográfica que su pareja (excepto Sur de Brasil) con fines de jurisdicción fiscal y de aplicación de la ley.

## Grupos de recursos de Azure

Un grupo de recursos es un contenedor lógico para recursos implementados en Azure. Estos recursos pueden ser cualquier cosa que cree en una suscripción de Azure como máquinas virtuales, instancias de Azure Application Gateway y de Azure Cosmos DB. Todos los recursos deben estar en un grupo de recursos, y un recurso solo puede ser miembro de un único grupo de recursos. Muchos recursos pueden moverse entre grupos de recursos con algunos servicios que tengan limitaciones o requisitos determinados para mover. Los grupos de recursos no se pueden anidar. Antes de poder aprovisionar un recurso, necesita un grupo de recursos en el que colocarlo.

### Agrupación lógica

La agrupación lógica es el aspecto que más le interesa, ya que, entre los recursos, el desorden es elevado.

### Ciclo de vida

La organización de los recursos por ciclo de vida puede ser útil en entornos que no sean de producción, en los que puede probar un experimento y después descartarlo. Los grupos de recursos facilitan la tarea de quitar un conjunto de recursos a la vez.

### Autorización

Los grupos de recursos también son un ámbito para aplicar permisos de control de acceso basado en roles (RBAC).

## Azure Resource Manager

Es el servicio de implementación y administración para Azure que proporciona una capa de administración.

Cuando un usuario envía una solicitud de cualquiera de las herramientas, las API o los SDK de Azure, Resource Manager recibe la solicitud. Autentica y autoriza la solicitud. Resource Manager envía la solicitud al servicio de Azure, que lleva a cabo la acción solicitada. Dado que todas las solicitudes se controlan mediante la misma API, verá resultados y funcionalidades coherentes en todas las distintas herramientas.

![Diagrama que muestra un modelo de solicitud de Resource Manager.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/consistent-management-layer-feef9259.png)

### Ventajas de usar Administrador de recursos

Con Resource Manager puede:

- Administrar la infraestructura mediante plantillas declarativas en lugar de scripts. Una plantilla de Resource Manager es un archivo JSON que define lo que quiere implementar en Azure.
- Implementar, administrar y supervisar todos los recursos de la solución en grupo, en lugar de controlarlos individualmente.
- Vuelva a implementar la solución a lo largo del ciclo de vida de desarrollo y tenga la seguridad de que los recursos se implementan en un estado coherente.
- Definir las dependencias entre recursos de modo que se implementen en el orden correcto.
- Aplique control de acceso a todos los servicios, puesto que RBAC se integra de forma nativa en la plataforma de administración.
- Aplicar etiquetas a los recursos para organizar de manera lógica todos los recursos de la suscripción.
- Comprenda la facturación de la organización viendo los costos de un grupo de recursos que comparten la misma etiqueta.

## Suscripciones de Azure

a suscripción le proporciona acceso autenticado y autorizado a los servicios y productos de Azure. Una suscripción de Azure es una unidad lógica de servicios de Azure que está vinculada a una cuenta de Azure, que es una identidad en Azure Active Directory (Azure AD) o en un directorio en el que confía Azure AD.

![Diagrama que muestra las suscripciones de Azure usan la autenticación y la autorización para acceder a las cuentas de Azure.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/subscriptions-afe063a7.png)

Una cuenta puede tener una suscripción o varias suscripciones que con distintos modelos de facturación y a las que se aplican diferentes directivas de administración de acceso

- **Límite de facturación**: Este tipo de suscripción determina cómo se factura una cuenta de Azure por el uso de Azure. Puede crear varias suscripciones para diferentes tipos de requisitos de facturación. Azure genera facturas e informes de facturación independientes para cada suscripción, de modo que pueda organizar y administrar los costos.
- **Límite de control de acceso**: Azure aplica las directivas de administración de acceso en el nivel de suscripción, por lo que puede crear suscripciones independientes para reflejar distintas estructuras organizativas. Este modelo de facturación le permite administrar y controlar el acceso a los recursos que los usuarios aprovisionan con suscripciones específicas.

### Creación de una suscripción de Azure adicional

- **Entornos**: suscripciones con el fin de configurar entornos independientes para el desarrollo y las pruebas, para seguridad o para aislar los datos por motivos de cumplimiento.
- **Estructuras organizativas**: puede crear suscripciones para reflejar las distintas estructuras organizativas. Este diseño permite administrar y controlar el acceso a los recursos que los usuarios aprovisionan en cada suscripción.
- **Facturación**: suscripciones adicionales para fines de facturación. 

- **Límites de suscripción**: las suscripciones se enlazan a algunas limitaciones de hardware. Esos límites se deben tener en consideración al crear suscripciones en la cuenta.

### Personalización de la facturación para satisfacer sus necesidades

Si tiene varias suscripciones, puede organizarlas en secciones de la factura. Cada sección de la factura es un elemento de línea en la factura que muestra los cargos en los que se incurre ese mes.

En función de sus necesidades, se pueden configurar varias facturas dentro de la misma cuenta de facturación. Para ello, cree perfiles de facturación adicionales. Cada perfil de facturación contiene su propia factura mensual y método de pago.

![Diagrama de flujo en el que se muestra un ejemplo de configuración de una estructura de facturación, donde diferentes grupos como marketing o desarrollo tienen su propia suscripción de Azure, que se acumula en una cuenta de facturación de Azure de pago más grande de la empresa.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/billing-structure-overview-2c81a8ad.png)

## Grupos de administración de Azure

Los grupos de administración de Azure ofrecen un nivel de ámbito que está por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración y las condiciones de gobernanza se aplican a los grupos de administración. Todas las suscripciones dentro de un grupo de administración heredan automáticamente las condiciones que se aplican al grupo de administración. Los grupos de administración proporcionan capacidad de administración de nivel empresarial a gran escala con independencia del tipo de suscripciones que tenga. Todas las suscripciones de un único grupo de administración deben confiar en el mismo inquilino de Azure AD.

### Jerarquía de los grupos de administración y las suscripciones

Puede compilar una estructura flexible de grupos de administración y suscripciones para organizar los recursos en una jerarquía para una administración unificada de las directivas y el acceso. 

![Diagrama que muestra un ejemplo de un árbol de jerarquía de grupos de administración.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-architecture-fundamentals/media/management-groups-and-subscriptions-bba71896.png)

> Puede crear una jerarquía que aplique una directiva.

### Hechos importantes acerca de los grupos de administración

- Se admiten 10 000 grupos de administración en un único directorio.
- Un árbol de grupo de administración puede admitir hasta seis niveles de profundidad. Este límite no incluye el nivel raíz ni el nivel de suscripción.
- Cada grupo de administración y suscripción solo puede admitir un elemento primario.
- Cada grupo de administración puede tener muchos elementos secundarios.
- Todas las suscripciones y grupos de administración están dentro de una única jerarquía en cada directorio.

## Terminología y conceptos de Azure

### ¿Qué es App Service?

App Service es un servicio basado en HTTP que permite crear y hospedar muchos tipos de soluciones basadas en la Web sin necesidad de administrar la infraestructura.

### ¿Qué es Azure Marketplace?

Azure Marketplace es una tienda en línea que hospeda aplicaciones certificadas y optimizadas para ejecutarse en Azure.

