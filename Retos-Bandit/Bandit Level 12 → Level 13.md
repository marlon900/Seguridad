# Bandit Level 12 → Level 13

## Objetivo de nivel
La contraseña para el siguiente nivel se almacena en los datos del data.txt, que es un hexdump de un archivo que se ha comprimido repetidamente. Para este nivel puede ser útil crear un directorio bajo /tmp en que puede trabajar usando mkdir. Por ejemplo: mkdir /tmp/myname123. A continuación, copie el archivo de datos mediante cp y cámbiele el nombre mediante mv

## Datos de acceso al nivel
``` bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

## Solución
``` bash
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cat data.txt | xxd -r | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:~$ 
```
## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xxd | Nos comprime un archivo |
| zcat | Nos comprime un archivo |
| tar xO | Nos comprime un archivo |

## Referencias
[Hex dump - Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)