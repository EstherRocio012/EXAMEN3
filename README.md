# IISSI-2 IS: Examen de laboratorio

## Proyecto base suministrado

Este repositorio incluye el backend completo (carpeta `DeliverUS-Backend`) y el frontend de `owner` (carpeta `DeliverUS-Frontend-Owner`). Servirá como base para realizar el examen de laboratorio de la asignatura.

## Preparación del entorno

### a) Windows

* Abra un terminal y ejecute el comando `npm run install:all:win`.

### b) Linux/MacOS

* Abra un terminal y ejecute el comando `npm run install:all:bash`.

## Ejecución

### Backend

* Para **rehacer las migraciones y seeders**, abra un terminal y ejecute el comando

    ```Bash
    npm run migrate:backend
    ```

* Para **ejecutarlo**, abra un terminal y ejecute el comando

    ```Bash
    npm run start:backend
    ```

### Frontend

* Para **ejecutar la aplicación frontend de `owner`**, abra un nuevo terminal y ejecute el comando

    ```Bash
    npm run start:frontend:owner
    ```

## Depuración

* Para **depurar el backend**, asegúrese de que **NO** existe una instancia en ejecución, pulse en el botón `Run and Debug` de la barra lateral, seleccione `Debug Backend` en la lista desplegable, y pulse el botón de *Play*.

* Para **depurar el frontend**, asegúrese de que **EXISTE** una instancia en ejecución del frontend que desee depurar, pulse en el botón `Run and Debug` de la barra lateral, seleccione `Debug Frontend` en la lista desplegable, y pulse el botón de *Play*.


## Test

* Para comprobar el correcto funcionamiento de backend puede ejecutar el conjunto de tests incluido a tal efecto. Para ello ejecute el siguiente comando:

    ```Bash
    npm run test:backend
    ```
**Advertencia: Los tests no pueden ser modificados.**

## Problemas con los puertos

En ocasiones, los procesos de backend o frontend, con o sin depuración, pueden quedarse bloqueados sin liberar los puertos utilizados, impidiendo que puedan ejecutarse otros procesos. Se recomienda cerrar y volver a iniciar VSC para cerrar dichos procesos.


## Procedimiento de entrega

1. Borrar las carpetas **node_modules** de backend y frontend y **.expo** del frontend.
1. Crear un ZIP que incluya todo el proyecto. **Importante: Comprueba que el ZIP no es el mismo que te has descargado e incluye tu solución**
1. Avisa al profesor antes de entregar.
1. Cuando el profesor te dé el visto bueno, puedes subir el ZIP a la plataforma de Enseñanza Virtual. **Es muy importante esperar a que la plataforma te muestre un enlace al ZIP antes de pulsar el botón de enviar**. Se recomienda descargar ese ZIP para comprobar lo que se ha subido. Un vez realizada la comprobación, puedes enviar el examen.
  
Si no se siguen estos pasos de manera escrupulosa, cabe la posibilidad de que no se entregue nada o que el ZIP contenga cualquier cosa. 

## Enunciado
Tras el lanzamiento inicial de DeliverUS, los inversores han solicitado una nueva función que permita a los propietarios pinear sus restaurantes. Cada propietario puede fijar tantos restaurantes como desee.

Un propietario puede anclar restaurantes de dos maneras diferentes:

En el formulario de creación de restaurantes. Por defecto, no estará anclado, pero el propietario puede elegir anclarlo. Para ello, se debe proporcionar un Interruptor que funciona con una propiedad llamada anclado. Si el interruptor está marcado, el restaurante se creará como anclado. El backend espera que la propiedad pinned sea booleana y opcional. Si la propiedad no está presente, se creará como no anclado.
Tarea 1 Puntuación
RF1. Capacidad para crear un restaurante anclado o no anclado. (2 puntos)
RF2. Capacidad para establecer un restaurante existente como anclado o no anclado. (2 puntos)
RF3. Listar los restaurantes en el orden descrito: primero los restaurantes anclados ordenados por fecha de anclaje (los restaurantes anclados más antiguos deben ir primero), y luego los restaurantes no anclados. (1 punto)
Tarea 2 Puntuación
RF1. Capacidad para crear un restaurante anclado o no anclado. (1 punto)
RF2. Capacidad para establecer un restaurante existente como anclado o no anclado.
RF2.1. Posibilidad de fijar un restaurante existente, con confirmación e información sobre el éxito de la fijación. (1,5 puntos)
RF2.2. Posibilidad de desanclar un restaurante existente, con confirmación e información sobre el éxito del desanclaje. (1,5 puntos)
Global. Corrección visual: iconos, diseño, modales, etc. (1 punto)
Todas las acciones/pantallas/etc. que no puedan ser verificadas por humanos (como lo haría un usuario final) debido a cualquier error, no podrán ser consideradas para la puntuación.

En la pantalla "Mis restaurantes", a través de un icono que actuará como un botón y se mostrará junto a cada restaurante. Al pulsarlo, el restaurante se anclará o desanclará. La aplicación deberá pedir confirmación al propietario cuando se pulse el botón: utilice el componente ConfirmationModal proporcionado, similar al componente DeleteModal utilizado en la clase. El sistema informará al usuario si el restaurante ha sido anclado o desanclado.

Por último, los restaurantes anclados aparecerán siempre en la parte superior de la lista de restaurantes presentados a su propietario y se ordenarán por la fecha en que fueron anclados (los más antiguos primero), seguidos de los no anclados.
(Inglés)
