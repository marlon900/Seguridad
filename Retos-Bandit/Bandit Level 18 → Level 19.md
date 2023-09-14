# Bandit Level 18 → Level 19

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en un **archivo léame** en El directorio principal. Desafortunadamente, alguien ha modificado .**bashrc** para cerrar sesión cuando inicia sesión con SSH.

## Datos de acceso al nivel
``` bash
ssh bandit18@bandit.labs.overthewire.org -p 2220
bandit18
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```

## Solución
``` bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/cat readme

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Notas adicionales


## Referencias
