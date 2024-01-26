# Tipos de kernel y sus diferencias

## Kernel monolitico
Es un kernel de gran tamaño que puede gestionar todas las tareas. Se encarga de la gestion de memoria y procesos, asi como de la comunicacion entre los procesos y el soporte de las diferentes funciones de los drivers y el hardware

## Microkernel
Sirven para evitar el colapso total del sistema en caso de un fallo.

## Kernel hibrido
Combinacion entre el microkernel y el kernel monolitico. Puede ser modulado y es un kernel grande.

# User vs Kernel Mode

## User mode
En este modo un programa no puede acceder directamente a hardware o memoria del sistema

## Kernel mode
Aqui el sistema operativo y los controladores del dispositivo tienen acceso a todos los recursos del sistema, incluyendo el hardware y la memoria.

# Interruptions vs traps

## Interruptions
Estos se dan en cualquier momento por hardware o dispositivo periferico como la llegada de datos desde un teclado.

## traps
Son generados por el propio procesador o por el software en ejecucion como resultado directo de la ejecucion de una instruccion en el programa.

