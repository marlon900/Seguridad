# Bandit Level 21 → Level 22

## Objetivo de nivel
Un programa se ejecuta automáticamente a intervalos regulares desde **cron**, el programador de trabajos basado en el tiempo. Busque en /**etc/cron.d/** la configuración y ver qué comando se está ejecutando.

## Datos de acceso al nivel
``` bash
ssh bandit21@bandit.labs.overthewire.org -p 2220
bandit21
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```

## Solución
``` bash
bandit21@bandit:~$ ls  /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```
## Notas adicionales
| Comando | Descripción |
| ------ | ------ |
| cron | Permite programar comandos para que se ejectuten en algun momento indicado |

## Referencias
