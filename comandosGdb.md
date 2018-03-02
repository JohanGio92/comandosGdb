# Comandos de gbd

### Guia rapida para comenzar a depurar

_Trabajo en proceso_

- `g++ [nombreDelArchivo.cpp] -o [ejecutable] --debug --DTEST -g`: creamos ejecutable.
- `gdb + [ejecutable]`: abrimos el programa para depurar.
- `run`: corre el programa.
- `start`: el programa se ejecuta linea por linea.
- `next`: avanza a la siguiente linea.
- `enter`: ejecuta la anterior comando.
- `step`: entra a la implementacion una funcion.
- `continue`: continua hasta la siguiente breakpoint.
- `list [empiezaLinea], [terminaLinea]`: enlista las 10 primeras lineas si solo
usas "list", de lo contrario puedes determinar de donde hasta donde quieres enlistar.
- `break [numeroDeLinea or nombreDeFuncion]`: crea un punto de ruptura, es decir,
el programa empieza a correr hasta la linea donde creaste la ruptura.
- `delete [numero de ruptura]`: borra todos los breakpoint si se utiliza solo
"delete" o puedes borrar uno en especifico.
- `print [nombreVariable]`: imprime el valor de una funcion, variable, puntero, ect.
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
