# Bandit Level 6 → Level 7

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena **en algún lugar del y** tiene todas las propiedades siguientes:

- Propiedad del usuario Bandit7
- Propiedad de Group Bandit6
- 33 Bytes de tamaño

## Datos de acceso al nivel
```
ssh bandit6@bandit.labs.overthewire.org -p 2220
bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Solución
``` bash
bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$ 
```
## Notas adicionales


## Referencias
