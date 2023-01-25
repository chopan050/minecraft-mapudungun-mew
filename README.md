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

Respecto a los JSONs, lo único que debes saber es que cada línea contiene dos textos entre comillas: el de la izquierda es una "llave" y el de la derecha, su "valor". Para entenderlo, abre el archivo en_cl.json y mira, por ejemplo, el 5° par llave-valor:
```json
"narrator.button.language": "Language",
```
La llave, "narrator.button.language", es una propiedad que lee Minecraft internamente: **la llave NO debe modificarse**. En este caso, cuando Minecraft lee la propiedad "narrator.button.language", encuentra el valor "Language". Por lo tanto, sabe que en pantalla debe mostrar el texto "Language" en el lugar que corresponda. Por lo tanto, **es este valor el texto que debe modificarse**.

"Language", que es "Idioma" en inglés, se traduce al mapudungun como "Kewün". Así, en arn_cl.json, se debería modificar el 5° par llave-valor para que diga:
```json
"narrator.button.language": "Kewün",
```

**Haz esto mismo con todas las líneas que sepas traducir en arn_cl.json. ¡Así es cómo traducimos Minecraft al mapudungun!**

...bueno, casi. Hay un detalle: en realidad no podemos poner "Kewün" en arn_cl.json, porque no podemos poner directamente la letra "ü" en el archivo. Si hacemos eso, Minecraft lo leerá mal y mostrará cualquier cosa en pantalla. En vez de poner ü, debesmos \u00fc. Aquí, \u indica que ingresaremos un carácter Unicode. En este caso, ingresamos el carácter cuyo número Unicode es 00fc, el cual corresponde a ü. Por lo tanto, lo correcto sería poner:
```json
"narrator.button.language": "Kew\u00fcn",
```
En mapudungun, en el grafemario Unificado, hay 4 caracteres a los cuales ponerle ojo. En vez de escribirlos directamente, deberías escribir lo que indicaremos a la derecha del carácter:
- Ü - \u00dc
- ü - \u00fc
- Ñ - \u00d1
- ñ - \u00f1

**¿Encuentras que esto es muy complicado? ¡No te preocupes! Escribe el texto normalmente, usando ü y ñ, y nosotros lo arreglamos manualmente cuando subas tus cambios.**

**Para modificar arn_cl.json, haz click en el archivo y luego busca el botón con un icono de lápiz a la esquina de arriba a la derecha de la caja de texto. Luego escribe todos los cambios que quieras realizar en el archivo. Una vez que termines con tus cambios por el momento, baja hasta el fondo de la página, ponle un nombre descriptivo a estos cambios (ejemplos: "Se tradujo la propiedad "narrator.button.language" o "Se tradujo todas las propiedades de narrator") y presiona en "Commit changes" para guardar todos tus cambios.**
