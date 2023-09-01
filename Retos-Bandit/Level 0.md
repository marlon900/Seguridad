# Level 0
## Objetivo de nivel

El objetivo de este nivel es que inicies sesión en el juego usando SSH. El host al que necesita conectarse es **bandit.labs.overthewire.org**, en el puerto 2220. El nombre de usuario es bandit0 y la contraseña es **bandit0**. Una vez Inicie sesión, vaya a la página de [Nivel 1](https://overthewire.org/wargames/bandit/bandit1.html) para averiguar cómo superar el Nivel 1.

## Datos de acceso al nivel
```
Server   : bandit.labs.overthewire.org
User     : bandit0
Password : bandit0
```
## Solución
``` bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Notas adicionales
| Comando | Descripción |
|---------|----------|
| pwd | me indica el directorio actual |
| whoami | saber el usuario actual |
| cd/ | me lleva al directorio raiz |
| ls | lista los archivos en la carpeta actual |

## Referencias