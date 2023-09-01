# Bandit Level 7 → Level 8

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt junto a la palabra **millionth**

## Datos de acceso al nivel
```
ssh bandit7@bandit.labs.overthewire.org -p 2220
bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

## Solución
``` bash
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```
## Notas adicionales
Utilizamos el comando "grep" para encontrar la palabra millionth, y así encontrar la contraseña.

## Referencias
https://www.hostinger.es/tutoriales/comando-grep-linux