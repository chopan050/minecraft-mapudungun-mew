# minecraft-mapudungun-mew

Mari mari!

Este proyecto está diseñado para Minecraft 1.19 y 1.19.2.

(OJO: ¡LA TRADUCCIÓN SIGUE EN PROGRESO!)

## Descargar y usar

Puedes presionar el botón verde "Code" y luego en "Download ZIP" para descargar el proyecto en un ZIP. También puedes clonar el repositorio si lo deseas.

Extrae el archivo. Deberías tener una carpeta llamada "minecraft-mapudungun-mew", que dentro contiene una carpeta "assets" entre otras cosas.

Busca dónde se encuentra la carpeta de Minecraft (en Windows puedes presionar Windows + R y escribir %appdata%, luego entrar a la carpeta llamada .minecraft). Ahí, entra a la carpeta resourcepacks y copia la carpeta minecraft-mapudungun-mew ahí dentro. (Si quieres, puedes cambiarle el nombre a "Minecraft Mapudungun Mew" o algo por el estilo)

¡Y listo! Ahora puedes abrir Minecraft 1.19 o 1.19.2, ir a Opciones -> Paquetes de recursos y seleccionar este paquete.

Una vez que actives este paquete, anda a Opciones -> Idioma y busca entre los primeros idiomas en la lista. El mapudungun debería ser el tercero en la lista.

## Colaborar

¡Muchas gracias por tu apoyo a este proyecto! **No necesitas tener conocimientos de programación** para colaborar en este proyecto.

La manera más sencilla de colaborar, la cual requiere menos conocimientos de Git, es haciendo todo desde la misma página de GitHub. (Si tienes más experiencia y te acomoda más, puedes clonar el repositorio y trabajar localmente, pero como este proyecto no requiere programar ni nada complejo, no es necesario esto)

### Instrucciones

**1. Crea tu propio fork de este repositorio.** En la esquina de arriba a la derecha, busca el botón "Fork" y hazle click. Una vez ahí, presiona "Create fork" para crear tu fork del repositorio.

**2. Realiza tus cambios.** Una vez que estés en tu fork, haz click en la carpeta "assets", luego en "minecraft", y finalmente en "lang". Ahí encontrarás tres archivos importantes en formato JSON:

- en_us.json: Contiene todos los textos originales de Minecraft en inglés. Este archivo no se modifica: está ahí de referencia.
- es_cl.json: Contiene los textos de Minecraft traducidos al español de Chile. Tampoco se modifica: es de referencia. **IMPORTANTE:** los caracteres á, é, í, ó, ú, ü y ñ están codificados. Por ello, vas a ver varios caracteres como \u00f1 que van a hacer difícil la lectura. **ADVERTENCIA: está en un orden distinto a en_us,json y arn_cl.json, lo cual puede ser confuso.**
- arn_cl.json: **Este es el archivo que debes modificar.** Debe contener los textos de Minecraft traducidos al mapudungun.

Respecto a los JSONs, lo único que debes saber es que cada línea contiene dos textos entre comillas: el de la izquierda es una "llave" y el de la derecha, su "valor". Miremos por ejemplo el 5° par llave-valor de "en_cl.json":
```json
"narrator.button.language": "Language",
```
La llave, "narrator.button.language", es una propiedad que lee Minecraft internamente: **la llave NO debe modificarse**. En este caso, cuando Minecraft lee la propiedad "narrator.button.language", encuentra el valor "Language". Por lo tanto, sabe que en pantalla debe mostrar el texto "Language" en el lugar que corresponda. Por lo tanto, **es este valor el texto que debe modificarse**. Así, en arn_cl.json, la línea correspondiente debería ser:
```json
"narrator.button.language": "Dungun",
```

