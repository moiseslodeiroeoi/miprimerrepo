# Ejercicios en grupo para entender Git/GitHub

Este es un ejercicio que funciona mejor con 3 ó 4 personas, trabajando desde un único repositorio git. 
El objetivo es demostrar de forma sencilla cómo git trata las fusiones de archivos/ramas, y cómo surgen los conflictos de fusión (y cómo arreglarlos, claro).

Cada grupo va a practicar el flujo de git visto en clase, siendo creativos :-)

## Pasos preparatorios:

* Nombrar un propietar@ del repositorio (crear uno aparte, mejor)
* Crear un repo en github
* Añadir a los miembros/as del grupo como colaboradores en el repositorio
* El **propietario/a** del repositorio debe iniciar el ejercicio clonando el repositorio y creando dos archivos (minion.md y one-line.md) en una rama local.
* minion.md debe tener una introducción de una línea ("¡Banana!" o similar) en la línea uno, y una línea de despedida ("¡Papaya!") sin embargo, la parte importante es dejar tres líneas en blanco para cada miembro del grupo. En un grupo de cuatro personas, la línea 1 dirá "¡Banana!", las líneas 2-13 estarán en blanco, y la línea 14 tendrá un mensaje de despedida.
* one-line.md debería tener un mensaje "¡Banana!" en la línea 1, y **una sola línea de texto en la línea 2** ("Baboi!").
* El propietario del repositorio debe guardar estos archivos y subirlos a una rama remota, y crear una solicitud de pull request a la rama principal. Alguien más debería revisarla y aprobarla (como pasa en la vida real ;-) ;-) ) 

## Que comiencen los juegos del calam.. hambre!

* Cada miembro/a del grupo debe clonar el repositorio (o sacar una copia nueva, si ya lo han clonado).
* El propietario del repositorio asigna a cada miembro del grupo un bloque de tres líneas vacías para trabajar (2-4, 5-7, 8-10, 11-13).
* Cada miembro del grupo escribe un minion en sus tres líneas asignadas entre el mensaje de "Banana" y el mensaje de "Papaya".
* Un [minion ipsum](https://www.minionsipsum.com) es un lorem ipsum pero con más gracia.
* Una vez que cada miembro del grupo haya escrito su obra maestra (banana? iiiii tatata bala tu uuuhhh hahaha), deberá guardarla y enviarla a una rama remota del repositorio.
* Todo el mundo debe crear pull requests a la vez - Esto simula el peor caso posible de cuatro personas tratando de alterar el mismo archivo al mismo tiempo (y pasa, créanme)
* Una vez que las solicitudes de pull han sido creadas, cada miembro del grupo debe revisar por turno las solicitudes de fusión.
* Como verás, al fusionar, github puede fusionar automáticamente todas y cada una de las solicitudes, sin problemas, porque puede detectar que los cambios en los archivos no están borrando nada, y no están sobrescribiendo nada que haya sido confirmado desde que se creó la solicitud de extracción.
* Pero ¡cuidado!, este es el mejor escenario para los conflictos de fusión - la razón por la que deberías sacar y fusionar copias maestras en la rama local antes de enviar confirmaciones es que la mayoría de los conflictos de fusión implican que la gente borre o altere el trabajo de otros.

## Segunda ronda

La segunda ronda comienza de la misma manera. Esta vez, el grupo trabaja en el archivo one-line.md al mismo tiempo.
* Cada miembro del grupo debe sacar la rama master actualizada, y sobrescribir la línea 2 con algo - cualquier cosa - que se le ocurra (manduca?)
* Guarden los cambios y envíenlos al origen remoto, y luego creen pull requests simultáneos.
* Mientras se turnan para fusionar la solicitud de extracción de otra persona con la rama maestra, notarán que la primera fusión está bien - ¡Github no tiene ningún problema con la gente que sobrescribe archivos!
* Sin embargo, el segundo intento de fusionar la solicitud de extracción de otra persona causará un error. Github le indicará que no puede fusionar automáticamente la solicitud, y que tendrá que resolver el problema en su rama local.
* Esto se debe a que github ve cuatro pull requests, intentando comparar con un archivo maestro (llamémoslo M, de Moi), pero en el momento en que la primera pull request se fusiona, M deja de existir - reemplazado por un archivo actualizado de una línea-prueba.md que llamaremos M1. El segundo pull request espera ser comparado con M, pero éste ya no existe, y github puede decir que está intentando sobrescribir una línea. En un programa de ordenador, esto podría causar un grave error, ya que la persona que crea la segunda solicitud de extracción podría no tener idea de que estaban tratando de sobrescribir M1, en lugar de M.
* Ahora cada miembro del equipo va a tener que tirar del nuevo master hasta su rama maestra local, fusionar el maestro con su rama local, y subir el resultado.
* Este proceso se repite una y otra vez. Como verán, cuatro personas podrían tardar casi diez minutos en resolver los problemas de intentar escribir una línea al mismo tiempo.
* Esperemos que después de esto, entiendas por qué es importante comprobar la rama master más actualizada antes de subir a una rama remota, y crear una solicitud de pull a la rama master.
* Puedes ejecutar esta prueba una segunda vez, con cada persona esperando a sacar la rama master actualizada, sobrescribiéndola en su rama local, y pusheando a una rama remota para crear un pull request a la maestra. 


Como verán, ¡un poco de comunicación y coordinación llega muy lejos! 
