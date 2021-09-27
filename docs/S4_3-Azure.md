# Azure modulo 2

## Introducción a los servicios de Azure Compute

Azure Compute es un servicio de informática a petición para ejecutar aplicaciones basadas en la nube. Solo se paga por los recursos que se usan y solo durante el tiempo que se usan, disponibles en minutos o segundos.

los servicios más destacados son los siguientes:

- Azure Virtual Machines
- Azure Container Instances
- Azure App Service
- Azure Functions (o *informática sin servidor*)

![Captura de pantalla de la página de servicios de proceso de Azure Portal, que incluye máquinas virtuales y contenedores.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-compute-fundamentals/media/compute-services-13e531e1.png)

### Maquinas Virtuales

Puede crear y utilizar máquinas virtuales en la nube. Virtual Machines proporciona infraestructura como servicio (IaaS) y se puede usar de maneras diferentes. Cuando necesite un control total sobre el entorno y el sistema operativo, las máquinas virtuales son la opción idónea.

### Azure Container Instances

Son un recurso de Azure Compute que puede usar para implementar y administrar un conjunto de máquinas virtuales idénticas. 

es más sencillo compilar servicios a gran escala cuyo destino sean las cargas de trabajo en contenedores, de macroproceso y macrodatos. A medida que la demanda aumente, se pueden agregar más instancias de máquina virtual. A medida que la demanda disminuya, se pueden quitar más instancias de máquina virtual. El proceso puede ser manual, automatizado o una combinación de ambos.

### Containers y Kubernetes

Son recursos de Azure Compute que puede usar para implementar contenedores y administrarlos. Los contenedores son entornos de aplicación ligeros y virtualizados. Están diseñados para crearse, escalarse horizontalmente y detenerse dinámicamente de forma rápida. Puede ejecutar varias instancias de una aplicación en contenedores en un único equipo host.

### Apps Services

Con Azure App Service puede compilar, implementar y escalar de forma rápida aplicaciones de API, móviles y web de nivel empresarial que se pueden ejecutar en cualquier plataforma. App Service es una oferta de plataforma como servicio (PaaS).

### Funciones

s una opción ideal si le preocupa solo el código que ejecuta el servicio y no la infraestructura o la plataforma subyacente. Se usan normalmente cuando se debe realizar un trabajo en respuesta a un evento (a menudo a través de una solicitud REST), un temporizador o un mensaje de otro servicio de Azure, y cuando ese trabajo puede completarse rápidamente, en segundos o en menos tiempo.

## Escalado de máquinas virtuales en Azure

Se pueden ejecutar máquinas virtuales únicas para pruebas, desarrollo o tareas secundarias. También se pueden agrupar las máquinas virtuales para proporcionar alta disponibilidad, escalabilidad y redundancia. Con independencia de cuáles sean los requisitos de tiempo de actividad. Estas características son:

- Conjuntos de escalado de máquinas virtuales
- Azure Batch

### ¿Qué son los conjuntos de escalado de máquinas virtuales?

Los conjuntos de escalado de máquinas virtuales permiten crear y administrar un grupo de máquinas virtuales idénticas, de carga equilibrada.

### ¿Qué es Azure Batch?

Azure Batch permite trabajo por lotes paralelos a gran escala y de informática de alto rendimiento (HPC) con la capacidad de escalar a decenas, cientos o miles de máquinas virtuales.

Cuando esté listo para ejecutar un trabajo, Batch:

- Iniciará un grupo de máquinas virtuales de proceso de forma automática.
- Instalará aplicaciones y datos de almacenamiento provisional.
- Ejecutará trabajos con tantas tareas como tenga.
- Identificará errores.
- Reordenará la cola de trabajo.
- Reducirá verticalmente el grupo a medida que se complete el trabajo.

## Azure App Service

### Tipos de servicios de aplicaciones

- Aplicaciones web
- Aplicaciones de API
- Trabajos web
- Aplicaciones móviles

App Service controla la mayoría de las decisiones sobre la infraestructura que se tratan en el hospedaje de aplicaciones accesibles desde la web:

- La implementación y administración se integran en la plataforma.
- Los puntos de conexión se pueden proteger.
- Los sitios se pueden escalar rápidamente para controlar cargas de tráfico elevado.
- El equilibrio de carga integrado y el administrador de tráfico proporcionan alta disponibilidad.

### Aplicaciones web

Incluye compatibilidad completa para hospedar aplicaciones web mediante ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP o Python. Puede elegir Windows o Linux como sistema operativo del host.

### Aplicaciones de API

Compilar API web basadas en REST mediante el lenguaje y el marco que prefiera. Se obtiene compatibilidad completa con Swagger y la posibilidad de empaquetar y publicar la API en Azure Marketplace. Las aplicaciones producidas se pueden consumir desde cualquier cliente basado en HTTP o HTTPS.

### Trabajos web

Se puede usar la característica WebJobs para ejecutar un programa (.exe, Java, PHP, Python o Node.js) o un script (.cmd, .bat, PowerShell o Bash) en el mismo contexto que una aplicación web, aplicación de API o aplicación móvil. Los puede programar o ejecutar un desencadenador. Los trabajos web suelen usarse para ejecutar tareas en segundo plano como parte de la lógica de aplicación.

### Aplicaciones móviles

Use la característica Mobile Apps de App Service a fin de compilar rápidamente un back-end para aplicaciones iOS y Android. Con unos pocos clics en Azure Portal, puede realizar lo siguiente:

- Almacenar los datos de aplicaciones móviles en una base de datos SQL basada en la nube.
- Autenticar a clientes con proveedores sociales comunes, como MSA, Google, Twitter y Facebook.
- Enviar notificaciones de inserción.
- Ejecutar lógica de back-end personalizada en C# o Node.js.

En el lado de la aplicación móvil, hay compatibilidad con el SDK para aplicaciones nativas de iOS y Android, Xamarin y React.

## Azure Container Instances o Azure Kubernetes Service

### ¿Qué son los contenedores?

Son un entorno de virtualización. Al igual que la ejecución de varias máquinas virtuales en un solo host físico, se pueden ejecutar varios contenedores en un solo host físico o virtual. A diferencia de las máquinas virtuales, no se administra el sistema operativo de un contenedor. Las máquinas virtuales parecen ser una instancia de un sistema operativo que se puede conectar y administrar, sin embargo los contenedores son ligeros y están diseñados para crearse, escalarse horizontalmente y detenerse de forma dinámica. Con los contenedores, puede reiniciar rápidamente en caso de bloqueo o interrupción del hardware.



### ¿Qué es Kubernetes?

Los contenedores se administran a través de un orquestador de contenedores, que puede iniciar, detener y escalar horizontalmente las instancias de la aplicación, según sea necesario. Hay dos maneras de administrar los contenedores basados en Microsoft y Docker en Azure: Azure Container Instances y Azure Kubernetes Service (AKS).

### ¿Qué es un microservicio?

Es un servicio web con ámbito reducido y bien definido y acoplado de forma flexible con otros servicios web.

## Azure Functions

es ideal si le preocupa solo el código que ejecuta el servicio, pero no la infraestructura o la plataforma subyacentes. Las funciones se usan normalmente cuando se debe realizar un trabajo en respuesta a un evento (a menudo a través de una solicitud REST), un temporizador o un mensaje de otro servicio de Azure, y cuando ese trabajo puede completarse rápidamente, en segundos o en menos tiempo.

## Azure Virtual Desktop

Es un servicio de virtualización de escritorios y aplicaciones que se ejecuta en la nube. Permite que los usuarios usen una versión hospedada en la nube de Windows desde cualquier ubicación. Azure Virtual Desktop funciona en dispositivos como Windows, Mac, iOS, Android y Linux. Funciona con aplicaciones que se pueden usar para acceder a aplicaciones y escritorios remotos. También puede usar la mayoría de los exploradores modernos para acceder a experiencias hospedadas en Azure Virtual Desktop.

## Aspectos básicos de Azure Virtual Network

### ¿Qué son las redes virtuales de Azure?

Las *redes virtuales de Azure* permiten a los recursos de Azure, como las máquinas virtuales, las aplicaciones web y las bases de datos, comunicarse entre sí, con los usuarios de Internet y con los equipos cliente en el entorno local.

Las redes virtuales de Azure proporcionan las importantes funcionalidades de red siguientes:

- Aislamiento y segmentación
- Comunicación con Internet
- Comunicación entre recursos de Azure
- Comunicación con los recursos locales
- Enrutamiento del tráfico de red
- Filtrado del tráfico de red
- Conexión de redes virtuales

#### Aislamiento y segmentación

Virtual Network permite crear varias redes virtuales aisladas. Al configurar una red virtual, se define un espacio de direcciones IP privadas con intervalos de direcciones IP públicas o privadas. Después, puede dividir ese espacio de direcciones IP en subredes y asignar parte del espacio de direcciones definido a cada subred con nombre

#### Comunicación con Internet

Una máquina virtual en Azure se puede conectar a Internet de forma predeterminada. Puede habilitar las comunicaciones entrantes desde Internet si define una dirección IP pública o un equilibrador de carga público. Para la administración de la máquina virtual, puede conectarse a través de la CLI de Azure, el Protocolo de escritorio remoto o Secure Shell.

#### Comunicación entre los recursos de Azure

Las redes virtuales de Azure permiten vincular entre sí los recursos del entorno local y dentro de la suscripción de Azure. Existen tres mecanismos para lograr esta conectividad:

- **Redes privadas virtuales de punto a sitio** el equipo cliente inicia una conexión VPN cifrada para conectar ese equipo a la red virtual de Azure.
- **Redes virtuales privadas de sitio a sitio** Una VPN de sitio a sitio vincula un dispositivo o puerta de enlace de VPN local con la puerta de enlace de VPN de Azure en una red virtual. La conexión se cifra y funciona a través de Internet.
- **Azure ExpressRoute** proporciona una conectividad privada dedicada a Azure que no viaja a través de Internet.

#### Enrutamiento del tráfico de red

De forma predeterminada, Azure enruta el tráfico entre las subredes de todas las redes virtuales conectadas, las redes locales e Internet. También puede controlar el enrutamiento e invalidar esa configuración del siguiente modo:

- **Tablas de rutas** Una tabla de rutas permite definir reglas para dirigir el tráfico. Puede crear tablas de rutas personalizadas que controlen cómo se enrutan los paquetes entre las subredes.
- **Protocolo de puerta de enlace de borde** El Protocolo de puerta de enlace de borde (BGP) funciona con puertas de enlace de VPN de Azure o con ExpressRoute para propagar las rutas BGP locales a las redes virtuales de Azure.

#### Filtrado del tráfico de red

- **Grupos de seguridad de red** Un grupo de seguridad de red es un recurso de Azure que puede contener varias reglas de seguridad de entrada y salida. Estas reglas se pueden definir para permitir o bloquear el tráfico en función de factores como el protocolo, el puerto y las direcciones IP de destino y origen.
- **Aplicaciones virtuales de red** Una aplicación virtual de red es una máquina virtual especializada que se puede comparar con un dispositivo de red protegido. Una aplicación virtual de red ejerce una función de red determinada, como ejecutar un firewall o realizar la optimización de la red de área extensa (WAN).

### Conexión de redes virtuales

Puede vincular redes virtuales entre sí mediante el *emparejamiento* de red virtual. El emparejamiento permite que los recursos de cada red virtual se comuniquen entre sí. Estas redes virtuales pueden estar en regiones distintas, lo que permite crear una red global interconectada con Azure.

UDR es enrutamiento definido por el usuario. Se trata de una actualización importante de las redes virtuales de Azure, ya que permite a los administradores de red controlar las tablas de enrutamiento entre las subredes de una red virtual, así como entre redes virtuales, lo que permite un mayor control sobre el flujo de tráfico de red.

![Ilustración de una puerta de enlace local o remota en una red virtual emparejada.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/local-or-remote-gateway-in-peered-virual-network-21106a38.png)

## Aspectos básicos de Azure VPN Gateway

Las redes privadas virtuales usan un túnel cifrado en otra red. El tráfico se cifra mientras viaja por la red que no es de confianza para evitar ataques de interceptación o de otro tipo.

### Puertas de enlace de VPN

Una puerta de enlace de VPN es un tipo de puerta de enlace de red virtual. Las instancias de Azure VPN Gateway se implementan en instancias de Azure Virtual Network y habilitan la conectividad siguiente:

- Conectar los centros de datos locales a redes virtuales a través de una conexión de *sitio a sitio*.
- Conectar los dispositivos individuales a redes virtuales a través de una conexión de *punto a sitio*.
- Conectar las redes virtuales a otras redes virtuales a través de una conexión *entre redes*.

![Visualización de una conexión VPN a Azure.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/vpngateway-site-to-site-connection-diagram-0e1e7db2.png)

#### Redes privadas virtuales basadas en directivas

Las instancias de VPN Gateway basadas en directivas especifican de forma estática la dirección IP de los paquetes que se deben cifrar a través de cada túnel. Este tipo de dispositivo evalúa cada paquete de datos en función de los conjuntos de direcciones IP para elegir el túnel a través del cual se va a enviar el paquete.

Entre las características clave de las instancias de VPN Gateway basadas en directivas en Azure se incluyen:

- Compatibilidad solo con IKEv1, que es se usa para establecer una asociación de seguridad (un contrato del cifrado) entre dos puntos de conexión.
- Uso del *enrutamiento estático*, en el que las combinaciones de prefijos de dirección de ambas redes controlan cómo se cifra y descifra el tráfico a través del túnel VPN. El origen y destino de las redes de túnel se declaran en la directiva y no necesitan declararse en las tablas de enrutamiento.
- Las redes privadas virtuales basadas en directivas se deben usar en escenarios específicos que las necesiten, por ejemplo, para ofrecer compatibilidad con dispositivos de red privada virtual locales heredados.

#### Redes privadas virtuales basadas en rutas

Si la definición de las direcciones IP que están detrás de cada túnel es demasiado compleja, se pueden usar puertas de enlace basadas en rutas. Con las puertas de enlace basadas en rutas, los túneles IPSec (protocolo de seguridad de Internet)  se modelan como una interfaz de red o una interfaz de túnel virtual. El enrutamiento IP (ya sean rutas estáticas o protocolos de enrutamiento dinámico) decide cuál de estas interfaces de túnel se va a usar al enviar cada paquete. Las redes privadas virtuales basadas en rutas son el método preferido para conectar dispositivos locales. Son más resistentes a los cambios de la topología, como la creación de subredes.

Si necesita alguno de los siguientes tipos de conectividad, use una instancia de VPN Gateway basada en rutas:

- Conexiones entre redes virtuales
- Conexiones de punto a sitio
- Conexiones de varios sitios
- Coexistencia con una puerta de enlace de Azure ExpressRoute

Entre las características clave de las instancias de VPN Gateway basadas en rutas en Azure se incluyen:

- Compatibilidad con IKEv2
- Uso de selectores de tráfico universales (comodín)
- Puede usar *protocolos de enrutamiento dinámico*, donde las tablas de enrutamiento y reenvío dirigen el tráfico a diferentes túneles IPSec. En este caso, las redes de origen y destino no se definen estáticamente como en las VPN basadas en directivas o incluso en las VPN basadas en rutas con enrutamiento estático. En su lugar, los paquetes de datos se cifran en función de las tablas de enrutamiento de red que se crean de forma dinámica mediante protocolos de enrutamiento, como el Protocolo de puerta de enlace de borde (BGP).

### Recursos de Azure necesarios para una VPN Gateway

Se necesitarán estos recursos de Azure para poder implementar una instancia de VPN Gateway operativa:

- **Red virtual**

- **GatewaySubnet**. Implemente una subred llamada `GatewaySubnet` para la instancia de VPN Gateway. Use al menos una máscara de dirección **/27** con el fin de asegurarse de que proporciona suficientes direcciones IP en la subred para un crecimiento futuro. Esta subred no se puede usar para otros servicios.

- **Dirección IP pública**. Cree una dirección IP pública dinámica de SKU básico si usa una puerta de enlace que no tenga en cuenta la zona

- **Puerta de enlace de red local**. Cree una puerta de enlace de red local para definir la configuración de la red local. Esta información la usa la instancia de VPN Gateway con el fin de enrutar paquetes destinados para las redes locales a través del túnel IPSec.

- **Puerta de enlace de red virtual**. Cree la puerta de enlace de red virtual para enrutar el tráfico entre la red virtual y el centro de datos local u otras redes virtuales.

- **Conexión**. Cree un recurso de conexión para crear una conexión lógica entre la instancia de VPN Gateway y la puerta de enlace de red local.

  - La conexión se realiza a las direcciones IPv4 del dispositivo VPN local, tal como define la puerta de enlace de red local.
  - La conexión se realiza desde la puerta de enlace de red virtual y la dirección IP pública asociada.

  Se pueden crear varias conexiones.

![Visualización de los requisitos de recursos para una instancia de VPN Gateway](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/resource-requirements-for-vpn-gateway-2518703e.png)

## Escenarios de alta disponibilidad

Hay varias opciones para asegurarse de que se tiene una configuración de tolerancia a errores.

### Configuración de activo-en espera

De forma predeterminada, las instancias de VPN Gateway se implementan como dos instancias en una configuración de activo-en espera, incluso si solo ve un recurso de VPN Gateway en Azure. Cuando el mantenimiento planeado o la interrupción imprevista afectan a la instancia activa, la instancia en espera asume de forma automática la responsabilidad de las conexiones sin ninguna intervención del usuario. Durante esta conmutación por error, las conexiones se interrumpen, pero por lo general se restauran en cuestión de segundos si se trata del mantenimiento planeado y en un plazo de 90 segundos en el caso de las interrupciones imprevistas.

![Visualización de la puerta de enlace de red virtual activa-en espera](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/active-standby-c4a3c14d.png)

### Activo/activo

Al incorporar compatibilidad con el protocolo de enrutamiento de BGP, también puede implementar puertas de enlace VPN en una configuración del tipo activo/activo. En esta configuración, se asigna una IP pública única a cada instancia. Después, se crean túneles independientes desde el dispositivo local a cada dirección IP. Se puede ampliar la alta disponibilidad mediante la implementación de un dispositivo VPN local adicional.

![Visualización de la puerta de enlace de red virtual activa-activa](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/dual-redundancy-d76100c9.png)

### Conmutación por error de ExpressRoute

consiste en configurar una instancia de VPN Gateway como una ruta segura de conmutación por error para las conexiones ExpressRoute. Los circuitos ExpressRoute tienen resistencia integrada. Sin embargo, no son inmunes a los problemas físicos que afectan a los cables que entregan conectividad ni a las interrupciones que afectan a la ubicación completa de ExpressRoute. En escenarios de alta disponibilidad, en los que existe un riesgo asociado a una interrupción de un circuito ExpressRoute, también puede aprovisionar una instancia de VPN Gateway que usa Internet como un método alternativo de conectividad. De este modo, puede garantizar que siempre haya una conexión a las redes virtuales.

## Aspectos básicos de Azure ExpressRoute

ExpressRoute le permite ampliar las redes locales a la nube de Microsoft mediante una conexión privada con la ayuda de un proveedor de conectividad.

La conectividad puede ser desde una red de conectividad universal (IP VPN), una red Ethernet de punto a punto o una conexión cruzada virtual a través de un proveedor de conectividad en una instalación de ubicación compartida. Las conexiones de ExpressRoute no pasan por la red pública de Internet. Esto permite a las conexiones de ExpressRoute ofrecer más confiabilidad, más velocidad, latencia coherentes y mayor seguridad que las conexiones normales a través de Internet. Para información sobre cómo conectar la red a Microsoft mediante ExpressRoute, consulte ExpressRoute connectivity models (Modelos de conectividad de ExpressRoute).

![Visualización en la que se muestra una introducción de alto nivel sobre el servicio Azure ExpressRoute](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/azure-expressroute-overview-5520731d.png)

Modelo de interconexión de sistemas abiertos (OSI):

- **Nivel 2 (L2)**: se trata del nivel de vínculo de datos, que proporciona una comunicación de nodo a nodo entre dos nodos de la misma red.
- **Nivel 3 (L3)**: se trata del nivel de red, que proporciona el direccionamiento y enrutamiento entre los nodos de una red de varios nodos.

### Características y ventajas de ExpressRoute

El uso de ExpressRoute como servicio de conexión entre Azure y las redes locales tiene varias ventajas.

- Conectividad de nivel 3 entre su red local y Microsoft Cloud a través de un proveedor de conectividad. La conectividad puede ser desde una red de conectividad universal (IP VPN), una red Ethernet de punto a punto, o una conexión cruzada virtual a través de un intercambio de Ethernet.
- Conectividad de servicios en la nube de Microsoft en todas las regiones dentro de la región geopolítica.
- Conectividad global a los servicios de Microsoft en todas las regiones con el complemento ExpressRoute Premium.
- Enrutamiento dinámico entre la red y Microsoft a través de BGP.
- Redundancia integrada en todas las ubicaciones de configuración entre pares para una mayor confiabilidad.
- El tiempo de actividad de conexión SLA.
- Compatibilidad con QoS de Skype para la empresa.

#### Conectividad de nivel 3

ExpressRoute proporciona conectividad de nivel 3 (nivel de dirección) entre la red local y la nube de Microsoft a través de asociados de conectividad. Estas conexiones pueden ser de una red punto a punto o universal. También puede tratarse de conexiones cruzadas virtuales a través de un intercambio.

#### Redundancia integrada

Cada proveedor de conectividad usa dispositivos redundantes para garantizar que las conexiones establecidas con Microsoft tengan alta disponibilidad. Puede configurar varios circuitos para complementar esta característica. Todas las conexiones redundantes se configuran con conectividad de nivel 3 para cumplir los Acuerdos de Nivel de Servicio.

#### Conectividad con los Servicios en la nube de Microsoft

ExpressRoute permite el acceso directo a los siguientes servicios en todas las regiones:

- Microsoft Office 365
- Microsoft Dynamics 365
- Servicios de proceso de Azure, como Azure Virtual Machines
- Servicios en la nube de Azure, como Azure Cosmos DB y Azure Storage

Office 365 se creó para tener acceso a él de forma segura y fiable a través de Internet. 

#### Conectividad local con Global Reach de ExpressRoute

Puede permitir que Global Reach de ExpressRoute intercambie datos entre los sitios locales si conecta los diferentes circuitos ExpressRoute. El tráfico de los centros de datos viajará a través de la red de Microsoft.

#### Enrutamiento dinámico

ExpressRoute usa el protocolo de enrutamiento Protocolo de puerta de enlace de borde (BGP). BGP se usa para intercambiar rutas entre las redes locales y los recursos que se ejecutan en Azure. Este protocolo permite el enrutamiento dinámico entre la red local y los servicios que se ejecutan en la nube de Microsoft.

### Modelos de conectividad de ExpressRoute

ExpressRoute admite tres modelos que puede usar para conectar la red local con la nube de Microsoft:

- Ubicación de CloudExchange
- Conexión Ethernet de punto a punto
- Conexión universal

![Visualización de modelos de conectividad de Azure](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-networking-fundamentals/media/azure-connectivity-models-4deabab1.png)

#### Coubicación en un intercambio en la nube

Normalmente, los proveedores de coubicación pueden ofrecer conexiones de nivel 2 y nivel 3 entre la infraestructura, que puede encontrarse en las instalación de la coubicación, y la nube de Microsoft. Por ejemplo, si el centro de datos tiene la ubicación compartida en un intercambio en la nube, como un ISP, puede solicitar una conexión cruzada virtual a la nube de Microsoft.

#### Conexión Ethernet de punto a punto

Las conexiones de punto a punto proporcionan conectividad de nivel 2 y nivel 3 entre el sitio local y Azure. Puede conectar sus oficinas o centros de datos a Azure mediante vínculos de punto a punto. Por ejemplo, si tiene un centro de datos local, puede usar un vínculo de Ethernet de punto a punto para conectarse a Microsoft.

#### Redes universales

Con la conectividad universal, puede integrar la red de área extensa (WAN) con Azure si proporciona conexiones a las oficinas y los centros de datos. Azure se integra con la conexión WAN para proporcionarle una conexión, como la que tendría entre el centro de datos y las sucursales.

Con las conexiones universales, todos los proveedores de WAN ofrecen conectividad de nivel 3. Por ejemplo, si ya usa la conmutación de etiquetas de multiprotocolo para conectarse a las sucursales o a otros sitios de la organización, una conexión ExpressRoute a Microsoft se comporta como cualquier otra ubicación en la WAN privada.

#### Consideraciones sobre la seguridad

Con ExpressRoute los datos no viajan a través de la red pública de Internet y, por tanto, no se exponen a los posibles riesgos asociados a las comunicaciones de Internet. ExpressRoute es una conexión privada de la infraestructura local a la infraestructura de Azure. Incluso si tiene una conexión ExpressRoute, las consultas de DNS, la comprobación de la lista de revocación de certificados y las solicitudes de Azure Content Delivery Network se siguen enviando a través de la red pública de Internet.

## Aspectos básicos de la cuenta de Azure Storage

Es un servicio que puede usar para almacenar archivos, mensajes, tablas y otros tipos de información. Los clientes como sitios web, aplicaciones móviles, aplicaciones de escritorio y muchos otros tipos de soluciones personalizadas pueden leer y escribir datos en Azure Storage. Azure Storage también se usa en máquinas virtuales de infraestructura como servicio y en servicios en la nube de plataforma como servicio.

Una cuenta de almacenamiento proporciona un espacio de nombres único para los datos de Azure Storage, al que se puede acceder desde cualquier lugar del mundo a través de HTTP o HTTPS. Los datos de esta cuenta son seguros, de alta disponibilidad, duraderos y escalables de forma masiva.

## Aspectos básicos de Disk Storage

Disk Storage proporciona discos para Azure Virtual Machines. Las aplicaciones y otros servicios pueden acceder a estos discos y usarlos cuando sea necesario

Los discos tienen diferentes tamaños y niveles de rendimiento, desde unidades de estado sólido (SSD) a unidades de disco duro (HDD)

## Aspectos básicos de Azure Blob Storage

Azure Blob Storage es una solución de almacenamiento de objetos para la nube. Puede almacenar grandes cantidades de datos, como datos de texto o binarios. Azure Blob Storage es no estructurado.

Los blobs no están limitados a formatos de archivo comunes. 

Blob Storage resulta ideal para lo siguiente:

- Visualización de imágenes o documentos directamente en un explorador.
- Almacenamiento de archivos para acceso distribuido.
- Streaming de audio y vídeo.
- Almacenamiento de datos para copia de seguridad y restauración, recuperación ante desastres y archivado.
- Almacenamiento de datos para el análisis en local o en un servicio hospedado de Azure.
- Almacenamiento de hasta 8 TB de datos para máquinas virtuales.

Los blobs se almacenan en contenedores, lo que ayuda a organizar los blobs en función de sus necesidades empresariales.

En el diagrama siguiente se muestra cómo puede usar las cuentas, los contenedores y los blobs de Azure.

![Diagrama de la jerarquía de una cuenta de almacenamiento](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-storage-fundamentals/media/account-container-blob-4da0ac47.png)

## Aspectos básicos de Azure Files
Azure Files ofrece recursos compartidos de archivos totalmente administrados en la nube a los que se puede acceder mediante los protocolos del Bloque de mensajes del servidor y Network File System (versión preliminar). Los recursos compartidos de Azure se pueden montar simultáneamente en implementaciones de Windows, Linux y macOS en la nube o locales. 

Use Azure Files para las siguientes situaciones:

- Muchas aplicaciones locales usan recursos compartidos de archivos. Azure Files facilita la migración de esas aplicaciones que comparten datos a Azure. Si monta el recurso compartido de archivos en la misma letra de unidad que usa la aplicación local, la parte de la aplicación que accede al recurso compartido de archivos debe funcionar con cambios mínimos, si los hay.
- Almacene archivos de configuración en un recurso compartido de archivos y acceda a ellos desde varias máquinas virtuales. Las herramientas y utilidades que usen varios desarrolladores de un grupo pueden almacenarse en un recurso compartido de archivos, lo que garantiza que todos los usuarios puedan encontrarlas y que utilizan la misma versión.
- Escriba datos en un recurso compartido de archivos y procese o analice los datos más adelante. Por ejemplo, puede que desee hacerlo con registros de diagnóstico, métricas y volcados de memoria.

La siguiente ilustración muestra el uso de Azure Files para compartir datos entre dos ubicaciones geográficas. Azure Files garantiza que los datos se cifren en reposo, y el protocolo SMB garantiza que los datos se cifren en tránsito.

![Diagrama en el que se muestran las funcionalidades de uso compartido de archivos de Azure Files entre un recurso compartido de archivos de Azure de Oeste de EE. UU. y otro de Europa, cada uno con sus propios usuarios de SMB.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/azure-storage-fundamentals/media/azure-files-5f942c3e.png)

Una cosa que distingue Azure Files de los archivos ubicados en un recurso compartido de archivos corporativo es que puede tener acceso a los archivos desde cualquier lugar del mundo mediante una dirección URL que apunte al archivo. También puede usar tokens de Firma de acceso compartido (SAS) para permitir el acceso a un recurso privado durante un período de tiempo determinado.

## Descripción de los niveles de acceso de blobs

Azure proporciona varios *niveles de acceso*, que puede usar para equilibrar los costos de almacenamiento con sus necesidades de acceso.

Entre los niveles de acceso disponibles se incluyen:

- **Nivel de acceso frecuente**: optimizado para almacenar datos a los que se accede con frecuencia (por ejemplo, imágenes para el sitio web).
- **Nivel de acceso esporádico**: optimizado para datos a los que se accede con poca frecuencia y que se almacenan al menos durante 30 días (por ejemplo, las facturas de los clientes).
- **Nivel de acceso de archivo**: conveniente para datos a los que raramente se accede y que se almacenan durante al menos 180 días con requisitos de latencia flexibles (por ejemplo, copias de seguridad a largo plazo).

Las siguientes consideraciones se aplican a los distintos niveles de acceso:

- Solo los niveles de acceso frecuente y esporádico se pueden establecer en el nivel de cuenta. El nivel de acceso de archivo no está disponible en el nivel de cuenta.
- Los niveles frecuente, esporádico y de archivo se pueden establecer en el nivel de blob durante la carga o después de esta.
- Los datos del nivel de acceso esporádico pueden tolerar una disponibilidad ligeramente inferior, pero aun así requieren una gran durabilidad, una latencia de recuperación y unas características de rendimiento similares a las de los datos de acceso frecuente. En el caso de los datos de acceso esporádico, un contrato de nivel de servicio (SLA) con una disponibilidad ligeramente inferior y unos costos de acceso mayores, en comparación con los datos de acceso frecuente, es aceptable a cambio de unos costos de almacenamiento menores.
- El almacenamiento de archivo almacena datos sin conexión y ofrece los menores costos de almacenamiento, pero los mayores costos de acceso y rehidratación de datos.