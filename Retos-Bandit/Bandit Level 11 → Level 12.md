# Bandit Level 11 → Level 12

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt, donde todas las letras minúsculas (a-z) y mayúsculas (A-Z) han sido rotado por 13 posiciones

## Datos de acceso al nivel
``` bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

## Solución
``` bash
bandit11@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit12 bandit11   49 Apr 23 18:04 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$ 
```
## Notas adicionales
| comando | descripción |
| ------ | ------ |
| tr | Indica como esta compuesto un conjunto |
| tr [[a-zA-Z]] [[n-za-mN-ZA-M]] | Rota las letras minusculas y mayusculas 13 posiciones |

## Referencias
[ROT13 - Wikipedia](https://en.wikipedia.org/wiki/ROT13)