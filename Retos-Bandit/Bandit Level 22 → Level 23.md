# Bandit Level 22 → Level 23

## Objetivo de nivel
Un programa se ejecuta automáticamente a intervalos regulares desde **cron**, el programador de trabajos basado en el tiempo. Busque en /**etc/cron.d/** la configuración y ver qué comando se está ejecutando.

**NOTA:** Mirar guiones de shell escritos por otras personas es un Habilidad muy útil. El script para este nivel se realiza intencionalmente Fácil de leer. Si tiene problemas para entender lo que hace, Intente ejecutarlo para ver la información de depuración que imprime.

## Datos de acceso al nivel
``` bash
ssh bandit22@bandit.labs.overthewire.org -p 2220
bandit22
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```

## Solución
``` bash
bandit22@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $myname
bandit23
bandit22@bandit:~$ mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
bandit22@bandit:~$ echo $mytarget
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit22@bandit:~$ cat /tmp/$mytarget
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit22@bandit:~$ 
```
## Notas adicionales
| Comandos | Descripción |
| ------------ | ------------- |
| cron | Permitite realizar una determinada tarea (o varias) en un determinado tiempo |

## Referencias
