# Resonando mensajes

Las primeras piezas de Vimscript que veremos son los comandos `echo` y `echom`.

Puede leer su documentación completa ejecutando `:help echo` y `:help echom` en Vim. A medida que vayas a través de este libro usted debe tratar de leer `:help` para cada comando nuevo que encuentre para aprender más sobre ellos.

Pruebe `echo` ejecutando el siguiente comando:

```vim
:echo "Hello, world!"
```

Usted debería ver `Hello, world!` aparecido en el final de la ventana.

## Eco persistente

Ahora, pruebe `echom` ejecutando el siguiente comando:

```vim
:echom "Hello again, world!"
```

Usted deberia ver `Hello again, world!` aparecido en el final de la ventana.

Para ver la diferencia entre estos dos comandos, ejecuta el siguiente comando:

```vim
:messages
```

Usted debería de ver un lista de mensajes. `Hello, world!` no estará es esta lista, pero `Hello again, world!` si estará.

Cuando escribas Vimscript más complicado más adelante en este libro, vas a desear "imprimir algo de salida" para ayudarte a depurar problemas. el comando `:echo` imprimirá la salida, pero a menudo desaparecera en el momento en que se haga el script. Usando `:echom` guardará la salida y podra ver los mensajes más tarde.

## Comentarios

Antes de seguir adelante, veamos cómo añadir comentarios. Cuando escribes codigo Vimscript (en tu archivo `~/.vimrc` o en cualquier otro) puedes añadir comentarios con el caracter `"`, de está manera:

```vim
" Make space more useful
nnoremap <space> za
```

Esto no siempre funciona (que es uno de esos rincones feos de Vimscript) Pero en la mayoría de los casos si funciona. Más adelante se hablará acerca de cuando no funciona (y por qué sucesede esto).

## Ejercicios

Leer `:help echo`.

Leer `:help echom`.

Leer `:help :messages`.

Agrega un linea en tu archivo `~/.vimrc` qué muestre un simpatico gato ASCII-art `(>^.^<)` cada vez que abra Vim.

