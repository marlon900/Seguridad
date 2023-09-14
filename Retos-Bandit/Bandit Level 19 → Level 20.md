# Bandit Level 19 → Level 20

## Objetivo de nivel
Para obtener acceso al siguiente nivel, debe usar el binario setuid en el directorio principal. Ejecútalo sin argumentos para averiguar cómo para usarlo. La contraseña para este nivel se puede encontrar en el habitual place (/etc/bandit_pass), después de haber utilizado el binario setuid.

## Datos de acceso al nivel
``` bash
ssh bandit19@bandit.labs.overthewire.org -p 2220
bandit19
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

## Solución
``` bash
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit20 bandit19 14876 Feb 21 22:03 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@bandit:~$ ./bandit20-do whoami
bandit20
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
## Notas adicionales


## Referencias
[Setuid - Wikipedia](https://en.wikipedia.org/wiki/Setuid)
