![Logo web](https://github.com/user-attachments/assets/76db2dd0-6b05-4efa-9565-6199850a91f1)

# ToList Web App to Manage tasks, in Kanban style.

![Desglose](https://github.com/user-attachments/assets/5faa0555-d814-4fdf-bbff-49743017b588)



La anterior fu un diagrama conceptual para la comprension de los requerimientos de la aplicacion y sus alcances

---

### Requerimientos:

- Formulario para crear una nueva tarea con campos para título, descripción y fecha de vencimiento.
- Validación de campos requeridos.
- Listado de tareas con información de título, descripción, fecha de vencimiento y estado (pendiente, en progreso, completada).
- Permitir marcar una tarea como completada.
- Permitir editar los detalles de una tarea.
- Permitir eliminar una tarea.
- Mostrar un resumen de las tareas pendientes, en progreso y completadas.
- Para mostrar la prueba desplegar en cualquiera de las siguientes opciones: firebase, netlify, github page, vercel entre otras…

---

![image](https://github.com/user-attachments/assets/602a30ff-b48f-4af6-8e87-39728b3ade14)

## Diseño del logo.svg

fuente de texto: Touvlo, con un check.

![image](https://github.com/user-attachments/assets/618ca5ee-dece-4719-87d5-87a8dde6d77c)


# Experiencia de Usuario de ToList

# Sobre las tareas y su gestion

tenemos tareas que son tipo kanban to do list
donde hay una seccion de tareas pendientes | Tareas en progreso | y Tareas completadas

- Este simbolo > aparecera para tareas pendientes, la flecha simboliza que sera empezada osease pasarla a un estado de **Tarea en progreso**
- Este simbolo ✓ aparecera para tareas en progreso, el check o chulo simboliza la posibilidad de marcar la tarea como completada cuando el usuario lo confirme.
- Este simbolo * * * o los famosos 3 puntos para demarcar que tiene un menu de opciones desplegables para:
	- eliminar totalmente
	- regresarla a tarea en progreso por que no se termino realmente
	- regresarla a pendientes pudiendo incluso reporgramar su fecha porque se debe realizar de nuevo
	- y otras opciones escalables.

basado en las convenciones de simbolos usados en el metodo Bullet Journal

## Interacciones

los simbolos se usaran para gestionar las tareas a traves de la secciones de to do list (pendientes, en progreso y completadas).

### Tarea pendiente

Empezar una Tarea pendiente o emprenderla mediante el simbolo disponible > como flecha, la cual sera la unica interaccion que permitira **ponerla en progreso**, se activara facilmente quizas agregue una notificacion para confirmar si de verdad el usuario va a emprender la tarea o sin querer su dedo lo acciono. ejemplo **¿Emprenderas esta Tarea?** **SI | NO**.
pues esto podria ser molesto si, pero tambien le da importancia y valor a cada tarea, no es toquetear y fingir que haremos todas estas tareas en progreso, que haya un esfuerzo y un cuestionamiento directo, para que sea como un ritual respetuoso hacia la tarea que el usuario se ha propuesto.

ordenar por predeterminado automaticamente las tareas segun su urgencia de fecha, y luego las que no la tienen fecha de vencimiento.

![Pasted image 20241121022404](https://github.com/user-attachments/assets/49dc5430-5b5e-4e64-b590-eade89b6cfff)


## Tarea en Progreso

El estado de una Tarea en progreso es importante comunicarlo, con enfasis, para que el usuario lo tenga presente como su miniproyecto concurrente, tampoco es que le demos colores llamativos ni nada, solo un color de enfasis de resalto, quizas no.
### Interacciones

el caso y lo importante es que al tocar el simbolo de interaccion **✓** este al contrario que al anterior, no tenga un mensaje de alterta de confirmacion, por el contrario tampoco sera un simple toqueteo y de una rapida e instantanea "listo completado!" , NO, al tocar el simbolo, este se rellenara por 3 segundos o menos hasta llenar el circulo de color con una animacion durante una sensacion de sostener el boton, cuando la animacion termine, expresar con colores como verde de aprobacion o mensaje directo sin ventana emergente de "Felicidades" o "Tarea Completada", haciendola desvanecer de la seccion de **Tareas en progreso**.

¿porque hacer algo tan molesto?, no lo es, es otro ritual, ocurre que es una alternativa al error de accionar la interaccion sin haber terminado la tarea realmente, y a su ves es una autocelebracion y confirmacion con orgullo de que, oye !termine una tarea muy laboriosa! y esta animacion que me hace sostenerla 2 segundos o menos con una bonita animacion de seguido me hace reforzar la evidencia de mi progreso. lo que motivara a traves del placer del cerebro a realizar la siguiente tarea. (esta opcion puede ser desactivada pero aspiro a cobrar al usuario por efectos de celebracion mas divertidas. manteniendo la simplicidad de la aplicacion).

## Tareas Completadas

en esta seccion estan las tareas completadas. es la que menos interaccion hay, pues solo tendra por cada tarea el tipico menu desplegable con opciones para reutilizar la tarea u regresarla a anteriores estados, asi mismo como eliminarla totalmente del registro. el  test no me pidio mucho en cuanto a eso. pero si pudiera lo mejoraria.

#  Interaccion ante la validacion de los campos.

![Pasted image 20241121005346](https://github.com/user-attachments/assets/35a5cf3e-874f-44d3-bbb4-800b972ee5c3)


se basa en To do list de micrososoft, normalmente todo list no te indica que debes escribir algo para poder hacerlo una tarea, el textbox al apretar enter o dar en en el boton de de interaccion si haber escrito un solo caracter, simplemente no hace nada, hasta que escribas algo.

Podria Hacerlo igual pero debo comunicarlo a traves de una animacion simple que se desvanezca rapido

La  fecha no se si es opcional pero no lo dejare a la suerte si la pedire, pero predeterminado dejare la fecha concurrente actual por si pasa de omision por el usuario.

## submenu

![Pasted image 20241121005927](https://github.com/user-attachments/assets/2cafffee-9fe8-4c40-8da7-b3eeaf1dff68)


el submenu se activa con el boton izquerdo en desktop, pero en movil solo con tener presionado mas de 1s la tarea, planeo que se exprese en forma de ventana emergente o modal centrado y de forma horizontal. sin opacar los demas contenidos, puesto que pidieron que se haga.
- Editar descripcion
- Eliminar tarea
Dependiendo del contexto de la tarea por ejemplo el caso de una tarea en progreso añadir la opcion.
- Regresar la Tarea a Pendientes | o | no realizare la tarea.
sea que al igual que pasa en el bullet journal, las tareas que no se puedan lograr porque son muy largas o tuvieron contratiempos y razones para ser realizadas pueden ser **Aplazadas** con una nueva fecha y directamente enviadas a tareas pendientes en una subseccion de Aplazadas.

> **En cualquier punto debe poderse eliminar y editar la descripcion, punto**


## Secciones de estado de Tareas,

se me ocurre usar las opciones de viñetas de navegacion, para emular un tablero kanban como pasar de derecha a izquierda para cambiar las secciones sin embargo se me piden dos cosas.
 - Un listado de Tareas con cada **estado** y el resto de su informacion
 - Un resumen de las tareas pendientes, en progreso y completadas, no se especifica como mostrarla, 
	 - pero planteo una metrica de "Hay demasiadas Tareas pendientes 😮 (color rojo)"; "Tienes varias Tareas en progreso 🧐 mirada juzgadora (color amarillo o zapote)"; "has completado una buena cantidad de tareas, sigue asi 😎 color (verde alegre)"
	 - Tambien podria mantenerse la idea de los colores para comunicar el descuido o la buena gestion de las tareas, pero solo se comunicaria sin juzgar al usuario con simples numeros:
		 - Pendientes (N) | En Progreso (N) | Completadas (N)
- La metrica reconoce el dia concurrente actual o semanal ante la cantida de Tareas formuladas y su movilidad de gestion o bueno solo la cantidad, no todas las tareas las haria el mismo dia. a menos que esas tareas esten programadas para un mismo dia, se podria involucrar el color rojo de alerta. o como sea.

Este Resumen se pondria al inicio superior centrado de la aplicacion sin molestar mucho, no al final. eso dependera de lo que se es conveniente pero en mi arquitectura de informacion me dice que comunicarlo al principio podria ser una buena idea con una fuente no muy explicita poco llamativa y el uso de los colores seria en la misma letra y se intensificaria segun lo que se deberia gestionar mas
- si hay muchas tareas pendientes, intensificarlos con un color rojo y los otros concepto mantener una degradacion del color menos enfocada.
- si hay muchas tareas en progreso enfocar con color degradado mas al centreo con color amarillo anaranjado de alerta, 
- si hay muchas tareas completadas en su balanza semana, pues se enfatizaria el color verde a ese extrema de las tres.

![Pasted image 20241121021855](https://github.com/user-attachments/assets/0f4fa766-9982-4462-a611-c10892db5443)

### como cuadrar las secciones to do list?

si bien el to do list, son las tres secciones que en modo de kanban es originalmente vertical, debo asegurar la señalizacion de como moverse a ellas desde la perspectiva first mobile o desde la perspectiva desktop.

hay un dilema, para movil hay dos opciones.
- 1. es scrollear verticalmente y separar las secciones con separadores horizontales, pero esta opcion sobrecarga el largor de la pagina verticalmente haciendo que las interacciones sean tediosas de ocurrir, podria apoyarse en despliegue unico de de secciones en esa forma pero se pierde mucho la magia.
- 2. Separar las secciones verticalmente apoyandose en una especie de carrusel de componentes, pasar el dedo verticalmente de extremos laterales de la pantalla hace posible eso, o usar botones laterales muy simples y que no invadan el contenido. este modelo permite que muchas interacciones tengan sentido. y la informacion es mas organizada. ejemplo:
	-  << ==Pendientes== | En Progreso | Completadas >>
	-  - Tarea pendiente #1 >
	-  - Tarea pendiente #2 >
- sea asi tambien navegar entre secciones al tocar esas flechas laterales o las secciones directamente, las dos formas son buenas opciones igualemente.


![Pasted image 20241121075855](https://github.com/user-attachments/assets/0b319462-9577-4db5-9c8d-adf95e6634e9)






