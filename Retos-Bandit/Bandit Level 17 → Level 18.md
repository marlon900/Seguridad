# Bandit Level 17 → Level 18

## Objetivo de nivel
Hay 2 archivos en el directorio de inicio: **passwords.old y passwords.new**. La contraseña para el siguiente nivel está en passwords.new y es la única línea que se ha cambiado entre **passwords.old y passwords.new**

**NOTA: si has resuelto este nivel y ves 'Byebye!' al intentar Para iniciar sesión en Bandit18, esto está relacionado con el siguiente nivel, Bandit19**

## Datos de acceso al nivel
``` bash
bandit17
ssh -i llave bandit17@bandit.labs.overthewire.org -p 2220
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```

## Solución
``` bash
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$ wc password.old
wc: password.old: No such file or directory
bandit17@bandit:~$ wc passwords.
passwords.new  passwords.old
bandit17@bandit:~$ wc passwords.old
 100  100 3300 passwords.old
bandit17@bandit:~$ wc passwords.new
 100  100 3300 passwords.new
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

bandit17@bandit:~$ 
```
## Notas adicionales


## Referencias
