# Comandos de gbd

### Guia rapida para comenzar a depurar

_Trabajo en proceso_

- `g++ [nombreDelArchivo.cpp] -o [ejecutable] --debug --DTEST -g`: creamos ejecutable.
- `gdb + [ejecutable]`: abrimos el programa para depurar.
- `display expression`: Importante usarlo, te muestra los valores de cada expression.
- `undisplay number`: elimina lo que muestra display y se usa un numero porque display crea un numero.
- `start`: el programa se ejecuta linea por linea.
- `run`: corre el programa.
- `continue`: continua hasta la siguiente breakpoint.
- `next`: avanza a la siguiente linea.
- `enter`: ejecuta la anterior comando.
- `step`: entra a la implementacion una funcion.
- `finish`: Es lo mismo que step out en los editores de texto.
- `list [empiezaLinea], [terminaLinea]`: enlista las 10 primeras lineas si solo
usas "list", de lo contrario puedes determinar de donde hasta donde quieres enlistar.
- `break [numeroDeLinea or nombreDeFuncion]`: crea un punto de ruptura, es decir,
el programa empieza a correr hasta la linea donde creaste la ruptura.
- `delete [numero de ruptura]`: borra todos los breakpoint si se utiliza solo
"delete" o puedes borrar uno en especifico.
- `print [nombreVariable]`: imprime el valor de una funcion, variable, puntero, ect.
- `print/x or print/t [nombreVariable]`: imprime el valor el hexadecimal o binario respectivamente
- `quit`: salida del programa.
- `info local`: despliega un informacion.
- `set`: fija un valor a la variable, ex: "set x = 5".
- `ptype [nombreDeLaVariable]`: devuelve el tipo de dato;
- `call`: similar al comando print solo que no despliega el valor devuelto.
- `watch [nombreVariable]`: se ve la informacion de la variable y como va cambiando.
- `generate-core-file`: crea un archivo donde se produce el core generado, luego
lo ejecutas junto con el arhivo que te genero core.
- `list [nombreDeArchivo]`: te muestra una lista de un archivo cuando hay
muchos archivos en gdb.
<!-- finish >
