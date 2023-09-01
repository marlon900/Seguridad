# Bandit Level 5 → Level 6

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en un archivo en algún lugar bajo El directorio **inhere**, y tiene todas las propiedades siguientes:

- legible por humanos
- 1033 Bytes de tamaño
- no ejecutable

## Datos de acceso al nivel
```
ssh bandit5@bandit.labs.overthewire.org -p 2220
bandit5
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

## Solución
``` bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU








                                        bandit5@bandit:~/inhere$ 
```
## Notas adicionales
Utilizamos el comando "find" para encontrar el archivo que necesitamos.

## Referencias
