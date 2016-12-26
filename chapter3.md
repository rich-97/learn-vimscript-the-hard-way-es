# Mapeo básico

Si hay una característica de Vimscript que le permitirá doblar Vim a su voluntad más que cualquier otro, es la capacidad de asignar claves. Las teclas de asignación le permiten decirle a Vim:

>   Cuando presione esta tecla, quiero que hagas estas cosas en lugar de lo que harías normalmente.

Vamos a empezar por mapear las teclas en modo normal. Hablaremos sobre cómo asignar claves en el modo de inserción y otros modos en el siguiente capítulo.

Escribe unas pocas lineas de texto dentro de un archivo, luego ejecuta:

```vim
:map - x
```

Coloca el cursor dónde sea en el texto y presione `-`. Observe cómo Vim elimina un caracter debajo del cursor, es cómo si presionaras `x`.

Ya tenemos una llave para "Eliminar el caracter debajo del cursor", así que vamos a cambiar esa asignación a algo un poco más útil. Ejecutar este comando:

```vim
:map - dd
```

Ahora coloca el cursor en un línea dónde sea y presiona `-` otra vez. Vim elimina la línea completa, por qué eso es lo que hace `dd`.

## Caracteres especiales

Puedes usar `<keyname>` para decirle a Vim acerca de las llaves especiales. Intenta ejecutar este comando:

```vim
:map <space> viw
```

Coloca el cursor sobre una palabra en tu texto y presiona la barra de espaciado.  Vim selecionará visualmente la palabra.

También puedes modificar el mapeo de llaves cómo `ctrl` y `alt`. Ejecuta esto:

```vim
:map <c-d> dd
```

Ahora presiona `Ctrl+d` en tu teclado será ejecuta `dd`.

## Comentando 

¿Recuerda en la primera lección dónde hablamos de los comentarios? El mapeo de llaves es uno de los lugares en dónde los comentarios no funcionan. Intenta ejecutar este comando:

```vim
:map <space> viw " Select word
```

Si tu intentas presionar la barra espaciadora ahora, algo horrible pasará El mapeo de llaves es uno de los lugares en dónde los comentarios no funcionan. Intenta ejecutar este comando:

```vim
:map <space> viw " Select word
```

Si tu intentas presionar la barra espaciadora ahora, algo horrible casi seguramente ocurrirá. ¿Por qué?

Cuando pulsas la barra de espacio ahora, Vim piensa que quieres que haga lo que `viw<space>"<espace>Select<space>word`. Obviamente esto no es lo que queremos.

Si observa de cerca el efecto de este mapeo puede notar algo extraño. Tómese unos minutos para tratar de averiguar exactamente qué sucede cuando lo usa, y por qué sucede.

No se preocupe si usted no lo consigue enseguida hablaremos de él más pronto.

## Ejercicios

Asigne la llave `-` para "Eliminar la línea actual, luego péguela debajo de la que estamos ahora". Esto permitirá mover líneas hacia abajo en su archivo con una pulsación de tecla.

Agrege ese comando de mapeo en tu archivo `~/.vimrc` entonces podrá usarlo en cualquier momento cuándo inice Vim.

Descubra cómo asignar la tecla `_` para mover la línea hacia arriba en lugar de hacia abajo.

Agregue esa asignación a su archivo `~/.vimrc` también.

Trate de adivinar cómo puede eliminar una asignación y restablecer una clave a su función normal.
