# Bandit Level 0 → Level 1
## Objetivo de nivel

La contraseña para el siguiente nivel se almacena en un archivo llamado **léame** ubicado en el directorio de inicio. Usar esta contraseña para iniciar sesión en bandit1 usando SSH. Siempre que encuentres una contraseña para un nivel, usa SSH (en el puerto 2220) para iniciar sesión en ese nivel y continuar el juego.

## Datos de acceso al nivel
```
bandit0
bandit0
```
## Solución
``` bash
bandit@bandit:~$ whoami
bandit0
bandit@bandit:~$ pwd
home/bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$ 
```

## Notas adicionales
| whoaim | me muestra el usuario actual |
| --------- | -------------------------------- |
| pwd | me muestra la carpeta actual |
| cat | muestra el contenido del archivo |

## Referencias
