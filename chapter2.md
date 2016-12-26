# Opciones de configuración

Vim tiene muchas opciones que puedes establecer para cambiar cómo se comporta.

Hay dos tipos principales de opciones: opción **Boolean** (ya sea "apagado" o "encendido") y las opciones que toman un valor.

## Opciones **Boolean**

Ejecute el siguiente comando:

```vim
:set number
```

La línea de números debería aparecer en el lado izquierdo de la ventana si no estaban activados. Ahora ejecute esto:

```vim
:set nonumber
```

La línea de números debería de desaparecer. `number` es una opción **Boolean**: puede estar apagada o encendida. Para cambiar cuándo este apagada la opción use `:set number` y para apagarla use `:set nonumber`.

Todas las opciones del tipo **Boolean** funciona de está manera. `:set <name>` para encender la opción y `:set no<name>` para apagar la opción.

## Alternar opciones **Boolean**

Tu tambien puedes "alternar" opciones **Boolean** para ponerlos al contrario de lo que son ahora. Ejecuta esto:

```vim
:set number!
```

La línea de números debería de reaparecer. Ahora ejecutalo de nuevo:

```vim
:set number!
```

Debería de desaparecer una vez más. Añade un `!` para alternar la opción **Boleean**.

## Revisando opciones

Tu puedes preguntar a Vim que opción está establecida usando `?`. Ejecuta estos comandos y mira que pasa después de cada uno:

```vim
:set number
:set number?
:set nonumber
:set number?
```

Notar cómo el primer comando `:set number?` muestra `number` mientras que el segundo mustra `nonumber`.

## Opciones con valores

Algunas opciones toman un valor en vez solo estar "apagada" o "encendida". Ejecuta los siguientes comandos y mira que pasa después de cada uno:

```vim
:set number
:set numberwidth=10
:set numberwidth=4
:set numberwidth?
```

La opción `numberwidth`  cambia la amplitud de la columna que contiene los números de línea. Tu puedes cambiar opciones **no-boolean** con `set <name>=<value>`, y revisarlas de la manera usual (`:set <name>?`).

Intenta revisar que otras opciones comunes esten establecidas:

```vim
:set wrap?
:set shiftround?
:set machtime?
```

## Configurando multiples opciones en una

Finalmente, tu puedes especificar más de una opción en el mismo comando `:set`. Intenta ejecutar esto:

```vim
:set numberwidth=2
:set nonumber
:set number numberwidth=6
```

Notar cómo ambas opciones se establecieron y tuvo efecto el ultimo comando.

## Ejercicios

Leer `:help 'number'` (Notar el entrecomillado).

Leer `:help relativenumber`.

Leer `:help numberwidth`.

Leer `:help wrap`.

Leer `:help shiftround`.

Leer `:help matchtime`.

Añade unas pocos lineas en tu archivo `~/.vimrc` para establecer estas opciones a tu gusto.
