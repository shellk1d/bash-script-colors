# Jet Black Matte Color Palette (en)

I'm attaching a color palette that I created using ANSI code to color the on-screen messages you want to print when you create your bash script. It's configuration-based "Jet Black Matte" from Obsidian's "Velocity".

```bash
# Delimiter and bold text
RESET='\e[0m'
BOLD='\e[1m'

# Text colors (cream tones)
MAIN='\e[38;2;232;225;206m'
SIDE='\e[38;2;190;185;170m'

# Colors for errors/warnings
DONE='\e[38;2;143;159;125m'
ALERT='\e[38;2;215;95;87m'
ERROR='\e[38;2;175;55;55m'
PROCESS='\e[38;2;210;140;110m'
COMMENTS='\e[38;2;110;105;95m'
```

For those who don't know how to use the color palette, the palette code is first declared at the start of the script. Then we use the following syntax:

```bash
...${COLOR} Hello world ${RESET}...
```

> [!IMPORTANT]
> It's important that you always put the ${RESET} variable at the end of the text you want to highlight, otherwise all subsequent messages printed on the screen will look the color you left unclosed.

I'm attaching a snippet of code that I always use in my scripts so you can see an example of typical usage that I give to this:

```bash
#########################################
# Custom color palette: Jet Black Matte #
#########################################

# Delimiter and blod text
RESET='\e[0m'
BOLD='\e[1m'

# Text colors (cream tones)
MAIN='\e[38;2;232;225;206m'
SIDE='\e[38;2;190;185;170m'

# Colors for errors/warnings
DONE='\e[38;2;143;159;125m'
ALERT='\e[38;2;215;95;87m'
ERROR='\e[38;2;175;55;55m'
PROCESS='\e[38;2;210;140;110m'
COMMENTS='\e[38;2;110;105;95m'

# Function in charge of canceling the execution of the program in case of doing CTRL+C.

function ctrl_c(){
  echo -e "\n\n${ERROR}[!] Error: Canceling execution...${RESET}\n"
  exit 1
}

# Redirect the program flow to the ctrl_c function.
trap ctrl_c INT
```


# Jet Black Matte Color Palette (es)

Te adjunto una paleta de colores que creé mediante código ANSI para darle color a los mensajes por pantalla que quieres imprimir cuando creas tu script de bash. Está basada en la configuración
"Jet Black Matte" del tema de Obsidian llamado "Velocity".

```bash
# Delimitador y texto en negrita
RESET='\e[0m'
BOLD='\e[1m'

# Colores de texto (tonos crema)
MAIN='\e[38;2;232;225;206m'
SIDE='\e[38;2;190;185;170m'

# Colores para errores/advertencias
DONE='\e[38;2;143;159;125m'
ALERT='\e[38;2;215;95;87m'
ERROR='\e[38;2;175;55;55m'
PROCESS='\e[38;2;210;140;110m'
COMMENTS='\e[38;2;110;105;95m'
```

Para aquellos que no saben cómo se usa la paleta de colores, primero se declara el código de la paleta al inicio del script. Después utilizamos
la siguiente sintaxis:

```bash
...${COLOR} Hola mundo ${RESET}...
```

> [!IMPORTANT]
> Es importante que siempre pongas la variable ${RESET} al final del texto que quieras resaltar, ya que de lo contrario, todos los siguientes mensajes que se impriman por pantalla se verán del color que dejaste sin cerrar.

Te adjunto un fragmento de código que siempre utilizo en mis scripts para que veas un ejemplo de uso típico que yo le doy a esto:

```bash
#############################################
# Paleta de colores custom: Jet Black Matte #
#############################################

# Limitador de color y negrita
RESET='\e[0m'
BOLD='\e[1m'

# Colores de texto (tonos crema)
MAIN='\e[38;2;232;225;206m'
SIDE='\e[38;2;190;185;170m'

# Colores de errores/advertencias
DONE='\e[38;2;143;159;125m'
ALERT='\e[38;2;215;95;87m'
ERROR='\e[38;2;175;55;55m'
PROCESS='\e[38;2;210;140;110m'
COMMENTS='\e[38;2;110;105;95m'

# Función encargada de cancelar la ejecución del programa en caso de hacer CTRL+C.

function ctrl_c(){
  echo -e "\n\n${ERROR}[!] Error: Cancelando ejecución...${RESET}\n"
  exit 1
}

# Redirgir el flujo del programa a la función ctrl_c
trap ctrl_c INT
```
