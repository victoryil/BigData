# Cloud Computing

Es un paradigma que permite ofrecer servicios de computación a través de una red, es decir, la disponibilidad a pedido de los recursos del sistema informático, sin gestión activa directa del usuario

El concepto de nube informática abarca todo los posibles servicios en línea, pero podemos dividirla en 3 modalidades que son las mas importantes y comunes:

- **SaaS:** Software como servicio, modelo de distribución en la que las aplicaciones están alojadas por una compañía o proveedor y puesta a disposición por estos.
- **PaaS:** Plataforma como servicio, conjunto de utilitarios para abastecer al usuario de S.O y servicios asociado a través de internet sin necesidad de descarga o instalación.
- **IaaS:** infraestructura como servicio, se refiere a la externalizar los equipos.
- ![Diagrama de los servicios separados por modelos de servicio en la nube.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/fundamental-azure-concepts/media/iaas-paas-saas-575a09e9.png)

### Características

Según la fuente que te proporcione estos servicios pueden variar pero las esenciales son las siguientes: 

- **Autoservicio bajo demanda:** provisión de medios sin interacción humana del proveedor de servicios
- **Acceso amplio y ubicuo a toda la red:** todos los recursos de los servicios se pueden acceder en cualquier dispositivo, como móvil, ordenador, etc..
- **Ubicación transparente y agrupación de recursos:** se puede especificar la ubicación del servicio, a nivel del país o estado.
- **Rápida elasticidad:** los recursos se aprovisionan y librean rápidamente según la demanda.
- **Servicio medido: ** se monitoriza el uso de recursos para controlar tanto el sistema, como para los costes, es totalmente transparente.
- **Autorreparable:** en caso de desperfecto, te brindan la opción de crear copias de seguridad automáticas de la ultima reservación de datos.
- **Agilidad:** capacidad de mejorar para ofrecer mejores recursos al cliente.
- **Costo:** la inversión inicial es menor con el cloud en nube a diferencia de la gran inversión de equipos locales.
- **Escalabilidad y elasticidad:** aprovisionamiento de recursos sobre una base de autoservicio sobre una base.
- **Virtualización:** facilita la migración entre servidores y libertad de manejo. 
- **Disponibilidad**
- **Rendimiento**
- **Seguridad**
- **Mantenimiento nulo**

### Tipo de PaaS

Anteriormente hablábamos de los principales tipos de servicios del cloud computing, en este caso vamos a dividir los tipos de Pass que nos podemos encontrar.

#### Públicos, privados e híbridos

Los privados son descargados e instalados en infraestructura local o nube publica y el hibrido es una mezcla entre el privado y el publico, siendo este en un servidor del proveedor.

#### Mobile PaaS

Proporciona capacidades de desarrollo para diseñadores y desarrolladores de aplicaciones móviles.

#### PaaS Abierto

Este no incluye alojamiento, sino que proporciona software de código abierto que permite a un proveedor PaaS ejecutar aplicaciones en un entorno de código abierto. 

#### PaaS para el Desarrollo Rápido

Plataformas empresariales públicas para desarrolladores rápidos como una tendencia emergente.

### Modelo de implementación

- **Nubes publicas:** nube computacional mantenida y gestionada por terceras personas no vinculadas con la organización.
- **Nubes privadas: ** buena si necesita alta protección de datos, accesible con VPN ya con algunos proveedores. Siendo el usuario propietario de los recursos.
- **Nubes hibridadas: **combina ambos modelos anteriores, el usuario es propietario de algunas partes y comparte otras.
- **Nube comunitaria: **se organiza con la finalidad de servir una función o propósito común, son administradas por las organizaciones a las que pertenece o terceras partes.

## Gastos de capital en comparación con los gastos operativos 

Hay dos tipos diferentes de gastos que se deben tener en cuenta:

- Los **gastos de capital (CapEx)** hacen referencia a la inversión previa de dinero en infraestructura física, que se podrá deducir a lo largo del tiempo. El costo previo de CapEx tiene un valor que disminuye con el tiempo.
- Los **gastos operativos (OpEx)** son dinero que se invierte en servicios o productos y se factura al instante. Este gasto se puede deducir el mismo año que se produce. No hay ningún costo previo, ya que se paga por un servicio o producto a medida que se usa.

### IaaS

#### Ventajas

**Sin gastos de capital (CapEx)**. Los usuarios no tienen costos iniciales.

**Agilidad**. Se pueden configurar las aplicaciones con rapidez para que sean accesibles y desaprovisionarlas cuando sea necesario.

**Administración**. Se aplica el modelo de responsabilidad compartida; el usuario administra y mantiene los servicios que ha aprovisionado, y el proveedor de nube administra y mantiene la infraestructura en la nube.

**Modelo basado en el consumo**. Las organizaciones solo pagan por lo que usan y operan en un modelo de gastos operativos (OpEx).

**Aptitudes**. No se requieren conocimientos técnicos avanzados para implementar y usar una nube pública u obtener las ventajas que esta ofrece. Las organizaciones pueden utilizar las aptitudes y la experiencia del proveedor de nube para asegurarse de que las cargas de trabajo sean seguras, estén protegidas y tengan alta disponibilidad.

**Ventajas que ofrece la nube**. Las organizaciones pueden utilizar las aptitudes y la experiencia del proveedor de nube para asegurarse de que las cargas de trabajo se configuren de forma que sean seguras y tengan alta disponibilidad.

**Flexibilidad**. IaaS es el servicio en la nube más flexible, ya que se dispone de control para configurar y administrar el hardware que ejecuta una aplicación.

### PaaS

PaaS proporciona las mismas ventajas y consideraciones que IaaS, pero ofrece algunas ventajas adicionales que es importante conocer.

#### Ventajas

**Sin gastos de capital (CapEx)**. Los usuarios no tienen costos iniciales.

**Agilidad**. PaaS es más ágil que IaaS, y no es necesario que los usuarios configuren servidores para ejecutar aplicaciones.

**Modelo basado en el consumo**. Los usuarios solo pagan por lo que usan y operan bajo un modelo OpEx.

**Aptitudes**. No se requieren conocimientos técnicos avanzados para implementar y usar una plataforma PaaS u obtener las ventajas que esta ofrece.

**Ventajas que ofrece la nube**. Los usuarios pueden aprovechar las aptitudes y la experiencia del proveedor de nube para asegurarse de que sus cargas de trabajo sean seguras y tengan alta disponibilidad. Además, los usuarios pueden obtener acceso a más herramientas de desarrollo punteras. Entonces, las podrán aplicar al ciclo de vida de una aplicación.

**Productividad**. Los usuarios se pueden centrar únicamente en el desarrollo de aplicaciones, ya que el proveedor de nube lleva a cabo toda la administración de plataformas. Trabajar con equipos distribuidos como servicios es más fácil, ya que se accede a la plataforma a través de Internet. Puede hacer que la plataforma esté disponible globalmente de forma más sencilla.

#### Desventaja

**Limitaciones de la plataforma**. Es posible que en las plataformas en la nube haya una serie de limitaciones que pueden afectar al modo en el que una aplicación se ejecuta. Al evaluar qué plataforma PaaS es más adecuada para una carga de trabajo, debe tener en cuenta las limitaciones de esta área.

### SaaS

SaaS es software que se hospeda y administra de forma centralizada para usted y sus usuarios o clientes. Normalmente se usa una versión de la aplicación para todos los clientes y la licencia se obtiene mediante una suscripción mensual o anual.

SaaS proporciona las mismas ventajas que IaaS, pero también ofrece algunas ventajas adicionales que es importante conocer.

#### Ventajas

**Sin gastos de capital (CapEx)**. Los usuarios no tienen costos iniciales.

**Agilidad**. Los usuarios pueden proporcionar al personal acceso al software más reciente de forma fácil y rápida.

**Modelo de precio de pago por uso**. Los usuarios pagan por el software que usan mediante un modelo de suscripción, que habitualmente es mensual o anual, independientemente de cuánto usen el software.

**Aptitudes**. No se requieren conocimientos técnicos avanzados para implementar y usar software SaaS u obtener las ventajas que este ofrece.

**Flexibilidad**. Los usuarios pueden acceder a los mismos datos de la aplicación desde cualquier lugar.

#### Desventaja

**Limitaciones de software**. Es posible que en las aplicaciones de software haya una serie de limitaciones que pueden afectar al modo en el que los usuarios trabajan. Como está usando el software tal cual, no tiene un control directo de las características. Al evaluar qué plataforma SaaS es más adecuada para una carga de trabajo, debe tener en cuenta cualquier necesidad empresarial y las limitaciones de software.

![Ilustración en la que se muestra el modelo de responsabilidad en la nube.](https://docs.microsoft.com/es-es/learn/azure-fundamentals/fundamental-azure-concepts/media/shared-responsibility-76efbc1e.png)

## ¿Qué es la informática sin servidor?

La informática sin servidor permite que los desarrolladores creen aplicaciones más rápidamente, ya que elimina la necesidad de administrar la infraestructura. En las aplicaciones sin servidor, el proveedor de servicios en la nube aprovisiona, escala y administra automáticamente la infraestructura necesaria para ejecutar el código. Las arquitecturas sin servidor son muy escalables y controla.
