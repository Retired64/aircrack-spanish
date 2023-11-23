## Aquí tienes algunos ejemplos de uso de `aircrack-ng` en diferentes casos:

1. **Crackeo de una red WEP:**

   ```bash
   aircrack-ng -a 1 -e Nombre_Red -b 00:11:22:33:44:55 archivo.cap
   ```
   Esto intentará crackear una red WEP con el nombre "Nombre_Red" y la dirección MAC del punto de acceso "00:11:22:33:44:55" utilizando un archivo de captura llamado `archivo.cap`.

2. **Crackeo de una red WPA-PSK con diccionario:**

   ```bash
   aircrack-ng -a 2 -e Nombre_Red -w diccionario.txt archivo.cap
   ```
   Intentará crackear una red WPA-PSK con el nombre "Nombre_Red" utilizando un diccionario de contraseñas llamado `diccionario.txt` y el archivo de captura `archivo.cap`.

3. **Crackeo de una red WPA-PSK con PMKID (hashcat -m 16800):**

   ```bash
   aircrack-ng -A -I PMKID_String -J salida.hccapx archivo.cap
   ```
   Utiliza el PMKID_String (obtenido previamente) para intentar crackear la red WPA-PSK y guarda los datos en un archivo HCCAPX llamado `salida.hccapx`.

4. **Realizar una prueba de velocidad de crackeo de WPA:**

   ```bash
   aircrack-ng -S -Z 60 archivo.cap
   ```
   Realiza una prueba de velocidad de crackeo de WPA en el archivo de captura `archivo.cap` durante 60 segundos para medir la velocidad de crackeo.

Recuerda que estos comandos son ejemplos y deben ser utilizados de manera ética y legal, idealmente en entornos controlados y con el permiso explícito del propietario de la red.
