# Bandit Level 2 → Level 3

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en un archivo llamado **espacios En este nombre de archivo** ubicado en el directorio principal

## Datos de acceso al nivel
```
ssh bandit2@bandit.labs.overthewire.org -p 2220
bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

## Solución
``` bash
bandit2@bandit:~$ pwd
/home/bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```

## Notas adicionales
Cuando un archivo cuenta con espacios en su nombre, no se puede acceder a el solo poniendo el nombre, deveras poner el nombre entre "", o también con un \ al final de cada palabra, exceptuando la última.

## Referencias
https://www.google.com/search?q=dashed+filename
http://tldp.org/LDP/abs/html/special-chars.html