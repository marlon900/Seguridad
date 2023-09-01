# Bandit Level 1 → Level 2

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en un archivo llamado **-** ubicado en el directorio de inicio.

## Datos de acceso al nivel
``` bash
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```

## Solución
``` bash
bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas adicionales
Cuando un archivo comienza con un ""-"",  para poder accederlo tenemos que anteponer un "./" al nombre o bien, especificar la ruta completa al archivo.

## Referencias
https://www.google.com/search?q=dashed+filename
http://tldp.org/LDP/abs/html/special-chars.html
