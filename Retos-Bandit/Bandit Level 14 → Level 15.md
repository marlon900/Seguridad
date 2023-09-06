# Bandit Level 14 → Level 15

## Objetivo de nivel
La contraseña para el siguiente nivel se puede recuperar enviando el Contraseña del nivel actual para el **puerto 30000 en localhost**.

## Datos de acceso al nivel
``` bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```

## Solución
``` bash
bandit14@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Apr 23 18:04 .
drwxr-xr-x 70 root root 4096 Apr 23 18:05 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
drwxr-xr-x  2 root root 4096 Apr 23 18:04 .ssh
bandit14@bandit:~$ nc -v localhost 30000
Connection to localhost (127.0.0.1) 30000 port [tcp/*] succeeded!
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
## Notas adicionales
| Comando | Descripción |
| ----------- | ------------- |
| nc | Se usa para llevar a cabo diversas tareas de red. |

## Referencias
[localhost - Wikipedia](https://en.wikipedia.org/wiki/Localhost)
[Comando nc (netcat): Qué es y cómo se usa | Neoguias](https://www.neoguias.com/comando-nc/)