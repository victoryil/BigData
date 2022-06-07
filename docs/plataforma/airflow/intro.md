# Airflow

Es una plataforma de administración de flujo de trabajo que le permite definir flujos de trabajo en el formulario del gráfico acíclico dirigido (**DAGs**) utilizando Python.

Python actua como el archivo de configuracion para el workflow, schedules y ejecucion de tareas definidas siguiendo las dependencias especificadas. Es altamente escalable y habilita un alto numero de workers.

## Componentes de Airflow

Airflow tiene 4 componentes principales: 

- UI / Web Server
- Scheduler
- Executer
- Metadata database

### Web Server

Provee una interfaz grafica a Airflow. Permite monitorear e interpretar los flujos de trabajos y mostrar si se han ejecutado correctamente o han fallado. También muestra los registros para que pueda comenzar a depurar a través del esfuerzo de la interfaz de usuario.

### Scheduler

Es el responsable de desencadenar los workflows y las tareas. Monitorea la tarea para saber si las dependencias están destinadas a activar la siguiente. También es responsable de mantenerse sincronizado con la carpeta donde se almacenan los DAGs de modo que pueda recoger nuevas etiquetas o cambios de código. Si el programador nota que la tarea debe activarse, se lo enviará al ejecutante que ejecutará la tarea.

### Executer

Es responsable de ejecutar realmente una tarea, determina cómo se deben administrar los recursos y qué trabajadores deben ejecutar cada tarea. Hay varios tipos de executer para diferentes casos de uso.

### Metadata database

Es una base de datos relacional donde el Scheduler y el Worker actualiza el estado sobre la ejecución de tareas

## Dags

Son colecciones de tareas o de trabajos a ejecutar conectados mediante relaciones y dependencias. Son la representación de los workflows.

Los grafos deben cumplir dos condiciones: ser dirigidos y acíclicos:

- **Dirigidos**: Las relaciones entre los nodos tienen solo un sentido.
- **Acíclicos**: No pueden formar ciclos, es decir, la ejecución no puede volver a un nodo que ya ha ejecutado.

Cada una de las tareas del DAG representada como un nodo, se describe con un **operador** y generalmente es atómica. Existen operadores predefinidos, y es posible extender y crear nuevos operadores si fueran necesarios.

### Default arguments

Es un diccionario que se analizará para todas las tareas, podemos pasar este diccionario al objeto DAGs, que lo pasará a todas las tareas.

Necesitaremos definir al menos dos argumentos para tu default arguments. El primero será el owner  y segundo la fecha de inicio.

## Tareas y operadores

### Tareas 

Representa un nodo en el gráfico. Es una unidad de trabajo que realizan los trabajadores. Una tarea siempre la define un operador.

### Operadores

Es la lógica real detrás de una tarea. Define qué tipo de acciones se realizan como parte de una tarea.

#### Tipos de operadores

- Operador de acción: realizan acciones o le dicen a un sistema que realice una acción.
- Operador de transferencia: este mueve los datos
- Sensores: siguen funcionando hasta que se cumple un criterio



Entre los operadores más usados se encuentran los siguientes:

- **Bash Operator**: Permite ejecutar scripts en Bash, aunque es posible modificarlo.
- **Database Operator**: Nos permite interactuar con bases de datos. Se usan al obtener datos de una base de datos mediante consultas SQL e información de autenticación. Es compatible con bases de datos populares como MySQL, Postgres, Sqlite o con JDBC.
- **Python Operator**: Ejecuta scripts en Python y operaciones creadas para el DAG.
- **Sensor Operator**: Está a la espera de detectar modificaciones en sistemas externos como ficheros o fuentes de datos.
- **Email Operator**: Este operador permite enviar un email a modo de notificación.
- **HTTP Operator**: Permite usar una API HTTP que necesite autenticación.

###  Definición de dependencias

cuando un operador depende de otro podemos indicarlo con *>>* o bien usando los metodos set_upstream y set_downstream

Ejemplo: El op2 dependerá de el op1. op1 >> op2 

### Arquitectura

![](assets/images/arch-diag-basic.png)

### Hooks

Se usa para conectarse con plataformas externas, los operadores usan hook por debajo. Mejora el rendimiento de las acciones cuando no están disponible via built-in operators. Se pueden usar en PythonOpterator

## XComs / Cross Cut Communication

Habilita el intercambio de mensajes, hace el push de clave valor desde una tarea a la base de datos de metadatos, comparte el estado.

Un X mensaje tiene clave, valor, task id, dag id, timestamp

