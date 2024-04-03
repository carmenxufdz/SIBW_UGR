# Practicas SIBW - UGR
Este repositorio contiene las prácticas realizadas para la asignatura Desarrollo de Sistemas de Información Basados en Web de la Universidad de Granada (UGR) del curso 2023/24. En estas prácticas se van implementando diferentes funcionalidades a la misma página, empezando por HTMP, CSS y Javascript, para terminar por PHP y AJAX. La implementación del código, así como el diseño escogido, es de creación propia.

## Práctica 1: HTML y CSS
El objetivo de esta práctica es el diseño de tres páginas con HTML + CSS, a saber:

* portada.html: La portadad de un sitio web que muestre información sobre posibles actividades en la montaña. El aspecto de la página debe ser similar al planteado en la figura 1:
    - Una zona de cabecera que deberá contener el nombre del sitio, algún logotipo y un menú horizontal.
    - Una zona lateral auxiliar donde aparecerán enlaces de interés.
    - Una zona principal donde se mostrarán fotos de las actividades de montaña junto con su nombre
    - Un pie con alguna nota de _Copyright_

* actividad.html: Vista en detalle de una de las actividades enlazadas desde la portada. La estructura de la página tiene elementos comunes con la portada, pero en la zona principal mostraremos información adicional de la actividad, por ejemplo:
    - Nombre de la actividad
    - Precio
    - Fotografía (o más de una), con su pie
    - Algunos párrafos describiendo la actividad
    - Botones o imágenes de redes sociales: al menos Facebook, Twitter e Imprimir
    - El botón Imprimir que llevará a la página actividad_imprimir.html

* actividad_imprimir.html: Contendrá la misma información que actividad.html pero formateada para la impresión de contenido. Es decir:
    - No dispondrá de menú de la cabecera ni el espacio auxiliar.
    - El logotipo se mostrará en otra posción.
    - Otra tipografía más clara
    - Fondo blaco, letra negra
    - Sin botones de redes sociales

![Figura 1](https://github.com/carmenxufdz/SIBW_UGR/blob/main/P1/esquema.jpg)

Para realizar lo que sería la estructura general de la página web: cabecera, menú, cuerpo y pie de página; utilicé un CSS en el que implemento cada uno de estas partes de la página web. Este CSS se utiliza tanto en la portada.html como en actividad.html. Además, para cada página implementé su propio CSS para el manejo del grid y la distribución de la página. 

En el menú horizontal, decidí crear un sub-menú desplegable para las actividades, y que al clickear en estas te llevasen también a la página principal; el menú Home que te llevará a portada.html; otro sub-menú desplegable para una página extra que creé de Montañar y un último menú no funcional para lo que sería una página de contacto.

![Portada](https://github.com/carmenxufdz/SIBW_UGR/blob/main/P1/portada.jpg)

![Actividad](https://github.com/carmenxufdz/SIBW_UGR/blob/main/P1/actividad.jpg)

Para actividad_imprimir.html utilizo un CSS diferente y propio para crear  un estilo de hoja de imprenta. Se usan fuentes más legibles y todo está en blanco y negro, incluido el logo.

![Imprimir](https://github.com/carmenxufdz/SIBW_UGR/blob/main/P1/imprimir.jpg)

## Práctica 2: Javascript
El objetivo de esta práctica es el diseño de un espacio para comentarios que los usuarios del sitio pueden hacer asociados a cada uno de las actividades mostradas en el sitio. Debe tener la siguiente funcionalidad:
* El panel de comentarios debe estar oculto en un lateral, y desplegarse al pulsar un botón
* Cuando se despliegue, deberá contar con dos comentarios predefinidos (como si hubieran sido introducidos por usuarios anteriores)
* Cada comentario tendrá autor, fecha y hora del comentario y texto del comentario
* Habrá un formulario con los siguientes campos:
    - Nombre
    - Email
    - Texto del comentario
    - Botón de enviar
* Al pulsar el botón de enviar, el texto del comentario se incluirá de forma similar a los ya existentes a continuación de estos usando JavaScript. Dichos comentarios desaparecerán al recargar la página.
* Al pulsar el botón de enviar, antes de incluir el texto del comentario se comprobará que todos los campos han sido rellenados. En caso negativo se avisará y no se incluirá el comentario. Además se realizará una validación de email
* Conforme el usuario escribe el comentario, el sistema detectará mediante JavaScript la apariciónde palabras "prohibidas". Cada uno de los caracteres de cada palabra prohibida se sustituirá por un * en tiempo de escritura

Para la resolución de esta práctica, tuve que crear e implementar un nuevo CSS con toda la estructura de la sección de comentarios. Para abrir y cerrar la sección, existe un botón "flotante" que se mantendrá a la izquierda de la página, a la derecha de la sección de comentarios.

´´´
function expandirComentarios(){
    if(abrir){
        cajaDesplegable.style.left="0"
        abrir=false;
    }
    else{
        cajaDesplegable.style.left="calc(-1 * min(600px, 55vw))"
        abrir=true;
    }
}
´´´

![Imprimi](https://github.com/carmenxufdz/SIBW_UGR/blob/main/P2/comentario.jpg)