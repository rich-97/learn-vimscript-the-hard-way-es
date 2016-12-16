# Prerequisitos

Para el uso de este libro debería tener la última versión de Vim instalada, la versión para este escrito será la 7.3. Las nuevas versiones de Vim son casi todas compatibles con versiones anteriores, Así qué cualquier cosa de este libro debería de funcionar correctamente con cualquier versión despues de 7.3 también.

Nada de este libro es específico para el Vim en consola o GUI Vims (IGU) como gVim o MacVim. Tú puedes usar el qué desees.

Tú deberias de estar cómodo editando archivos en Vim. Debe conocer la terminalogía básica de Vim como "buffer", "window", "normal mode", "insert mode" and "text object".

Si usted no está en ese punto todavía debe pasar por el programa vimtutor, Usar Vim exclusivamente durante un mes o dos, y volver cuando Vim se queme en tus dedos.

También necesitará tener algo de experiencia en programación. Si nunca has programado antes de salir aprende [Learn Python the Hard Way](https://learnpythonthehardway.org) primero y vuelve a este libro cuando hayas terminado.

## Creando un archivo Vimrc

Si ya conoces qué es un archivo `~/.vimrc` y tienes uno, dirigete hacia el próximo capítulo.

Un archivo `~/.vimrc` es un archivo que tu creas para que contenga un poco de código de Vimscript.

En linux y Mac OS X este archivo está ubicado en tu directorio *home* y se llama `.vimrc`.

En Windows este archivo está ubicado en tu carpeta *home* y se llama `_vimrc`.

Para buscar facilmente la ubicación y el nombre del archivo en cualquier sistema operativo, ejecuta `:echo $MYVIMRC` en Vim. La ruta será mostrada en el final de la pantalla.

Cree este archivo si aún no existe.

