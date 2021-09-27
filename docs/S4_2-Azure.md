# S4 - Azure

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

