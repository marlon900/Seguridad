# Bandit Level 8 → Level 9

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt y es la única línea de texto que aparece solo una vez.

## Datos de acceso al nivel
```
ssh bandit8@bandit.labs.overthewire.org -p 2220
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

## Solución
``` bash
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root    root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root    root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Apr 23 18:04 data.txt
-rw-r--r--  1 root    root      807 Jan  6  2022 .profile
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$ 
```
## Notas adicionales
Usamos Piping para resolver el problema, el cual se representa con un "|".

| sort | Ordena los archivos |
| ---- | ---------------------- |
| uniq | Muestra las veces que se repite un archivo |
## Referencias
https://ryanstutorials.net/linuxtutorial/piping.php