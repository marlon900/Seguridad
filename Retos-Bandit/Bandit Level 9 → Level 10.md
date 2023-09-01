# Bandit Level 9 → Level 10

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt en una de las pocas cadenas legibles por humanos, precedida por varios '=' Caracteres.

## Datos de acceso al nivel
```
ssh bandit9@bandit.labs.overthewire.org -p 2220
bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Solución
``` bash
bandit9@bandit:~$ ls -la
total 40
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit10 bandit9 19379 Apr 23 18:04 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit9@bandit:~$ cat data.txt | strings | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```
## Notas adicionales
El comando `strings` en Linux se utiliza para mostrar las secuencias de caracteres imprimibles que sean de al menos 4 caracteres de largo.

## Referencias
https://www.bing.com/search?pglt=41&q=que+hace+el+comando+strings+en+linux&cvid=19d2c14921b347619a9ac7c76fd634ee&aqs=edge..69i57j0l8.13409j0j1&FORM=ANNTA1&PC=SCOOBE&showconv=1