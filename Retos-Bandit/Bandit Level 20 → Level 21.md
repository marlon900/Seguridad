# Bandit Level 20 → Level 21

## Objetivo de nivel
Hay un binario setuid en el homedirectory que hace el Siguiendo: Realiza una conexión a localhost en el puerto que especifique como argumento de línea de comandos. A continuación, lee una línea de texto de la conexión y la compara con la contraseña del nivel anterior (bandido20). Si la contraseña es correcta, transmitirá el Contraseña para el siguiente nivel (Bandit21).

**NOTA:** Intente conectarse a su propio demonio de red para ver si funciona como piensas

## Datos de acceso al nivel
``` bash
ssh bandit20@bandit.labs.overthewire.org -p 2220
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```

## Solución
``` bash
bandit20@bandit:~$ nc -nlvp 8765 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[4] 3123078
bandit20@bandit:~$ Listening on 0.0.0.0 8765

bandit20@bandit:~$ ./suconnect 8765
Connection received on 127.0.0.1 60840
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ fg
nc -nlvp 8765 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
^C
```
## Notas adicionales


## Referencias
