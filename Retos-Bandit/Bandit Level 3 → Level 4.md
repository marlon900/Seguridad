# Bandit Level 3 → Level 4

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en un archivo oculto en el directorio **inhere**.

## Datos de acceso al nivel
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
bandit3
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Solución
``` bash
bandit3@bandit:~$ whoami
bandit3
bandit3@bandit:~$ pwd
/home/bandit3
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ pwd
/home/bandit3/inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr 23 18:04 .
drwxr-xr-x 3 root    root    4096 Apr 23 18:04 ..
-rw-r----- 1 bandit4 bandit3   33 Apr 23 18:04 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$ 
```
## Notas adicionales
Usamos la el parámetro -la con el comando ls para que nos muestre los archivos ocultos.

## Referencias
