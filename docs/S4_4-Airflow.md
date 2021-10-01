# Airflow

Es una plataforma de administración de flujo de trabajo que le permite definir flujos de trabajo en el formulario del gráfico acíclico dirigido (**DAGs**) utilizando Python.

Python actua como el archivo de configuracion para el workflow, schedules y ejecucion de tareas definidas siguiendo las dependencias especificadas. Es altamente escalable y habilita un alto numero de workers.

## Componentes de Airflow

![image-20211001095940396](C:\Users\vd.gil\AppData\Roaming\Typora\typora-user-images\image-20211001095940396.png)

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