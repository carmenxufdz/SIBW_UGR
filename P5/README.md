# Práctica 5: AJAX: Comunicación asíncrona con el servidor

## Descripción de la Práctica

Se nos ha solicitado una nueva funcionalidad:

* Cualquier persona podrá buscar actividades publicadas en el sitio. Conforme vaya tecleando en un campo de búsqueda (único, al estilo “Google”), se irán mostrando los nombres de las actividades que coincidan con dicha cadena de búsqueda. En caso de interesarle una de esas actividades, podrá acceder a la misma pulsando en el título mostrado.

* Un gestor del sitio podrá buscar de la misma manera entre todas las actividades, aunque no hayan llegado a publicarse. Hasta este momento no se había contemplado la posibilidad de que las actividades pudieran tener un estado “publicado” o “sin publicar”, por lo que habrá que realizar algunos cambios en el modelo de datos, así como en las consultas que se realicen sobre el mismo. Existen al menos dos posibilidades para hacer estos cambios que se deben analizar y/o adoptar:

    - Añadir un campo booleano en la tabla de actividades denominado publicado. En este caso, habrá que revisar nuestras consultas para devolver o no ese campo cuando sea necesario, así como revisar nuestras consultas (por ejemplo, cuando se listan las actividades) para mostrar solo los que tengan el estado publicado.

    - Crear una tabla nueva en la que se añadan o eliminen los identificadores de las actividades que sí están publicadas. En este caso, habrá que repasar las consultas que se hacen utilizando JOINs de las tablas (o varias consultas encadenadas).

Se considera obligatorio hacer que la modificación del estado publicado se tenga que realizar desde el panel de control del Gestor del sitio.