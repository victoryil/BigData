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