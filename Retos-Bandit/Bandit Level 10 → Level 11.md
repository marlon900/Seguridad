# Bandit Level 10 → Level 11

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt, que contiene datos codificados en base64

## Datos de acceso al nivel
```
ssh bandit10@bandit.labs.overthewire.org -p 2220
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Solución
``` bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ base64 -d data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ 
```
## Notas adicionales
usamos el comando base64 con el parámetro -d para decodificar el mensaje

## Referencias
https://en.wikipedia.org/wiki/Base64