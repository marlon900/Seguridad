# Bandit Level 13 → Level 14

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en /**etc/bandit_pass/bandit14 y sólo puede ser leída por el usuario bandit14**. Para este nivel, no obtienes la siguiente contraseña, pero obtener una clave SSH privada que se puede utilizar para iniciar sesión en el siguiente nivel. **Note: localhost** es un nombre de host que hace referencia a la máquina estás trabajando en

## Datos de acceso al nivel
``` bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

## Solución
``` bash
bandit13@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
-rw-r-----  1 bandit14 bandit13 1679 Apr 23 18:04 sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
The authenticity of host '[bandit.labs.overthewire.org]:2220 ([127.0.0.1]:2220)' can''t be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$
```
## Notas adicionales


## Referencias
[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)