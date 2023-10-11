## Objetivo While going through the deleted files of a coworker who was fired for selling information to a competitor recently, I came across an intriguing file. Although I can't decipher its content, I remember that he liked to learn Python in his spare time and once told me that he was interested in learning how to display binary data and compress information.

## Solución

Con el contenido del archivo hice dos códigos en python el primero es :

`import base64  encoded_data = "eJxLy0lM942o9k2syMwtzVUoTk0uLcosqVTILFaozC8tUijNS0ktKi5JzEvJzEtXyE9TKEpNzAEqqAUAgf8WPg==" decoded_data = base64.b64decode(encoded_data)  print(decoded_data)`

Con ese código decodificamos el texto que se nos da al principio y nos sale lo siguiente: b'x\x9cK\xcbIL\xf7\x8d\xa8\xf6M\xac\xc8\xcc-\xcdU(NM.-\xca,\xa9T\xc8,V\xa8\xcc/-R(\xcdKI-_.I\xccK\xc9\xccKW\xc8OS(JM\xcc\x01_\xa8\x05\x00\x81\xff\x16>' lo cual hice otro código para descomprimir en zlib:

`mport zlib  compressed_data = b'x\x9cK\xcbIL\xf7\x8d\xa8\xf6M\xac\xc8\xcc-\xcdU(NM.-\xca,\xa9T\xc8,V\xa8\xcc/-R(\xcdKI-*.I\xccK\xc9\xccKW\xc8OS(JM\xcc\x01*\xa8\x05\x00\x81\xff\x16>'  decompressed_data = zlib.decompress(compressed_data)  print(decompressed_data)`

Como resultado nos da: b'flagMX{Maximum security is your understanding of reality}' y la bandera es: flagMX{Maximum security is your understanding of reality}
