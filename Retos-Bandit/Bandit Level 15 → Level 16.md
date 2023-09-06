# Bandit Level 15 → Level 16

## Objetivo de nivel
La contraseña para el siguiente nivel se puede recuperar enviando el Contraseña del nivel actual para el **puerto 30001 en localhost** mediante Cifrado SSL.

**Nota útil: ¿Obtener "HEARTBEATING" y "Read R BLOCK"? Uso -ign_eof y lea la sección "COMANDOS CONECTADOS" en la página de manual. Junto a 'R' y 'Q', el comando 'B' también funciona en esta versión de ese comando ...**

## Datos de acceso al nivel
``` bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```

## Solución
``` bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
--------------------
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$ 
```
## Notas adicionales
| Comandos | Descripción |
| ------------ | ------------- |
| openssl | Se utiliza para administrar certificados, claves y realizar operaciones de seguridad |

## Referencias
[Transport Layer Security - Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
[OpenSSL Cookbook 3rd Edition (feistyduck.com)](https://www.feistyduck.com/library/openssl-cookbook/online/)
