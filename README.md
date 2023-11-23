## Manual de uso de `aircrack-ng`:

```
uso: aircrack-ng [opciones] <archivo(s) de entrada>

  Opciones comunes:

      -a <modo>  : forzar modo de ataque (1/WEP, 2/WPA-PSK)
      -e <essid> : selección de objetivo: identificador de red
      -b <bssid> : selección de objetivo: MAC del punto de acceso
      -p <nbcpu> : # de CPUs a utilizar (por defecto: todas las CPUs)
      -q         : habilitar modo silencioso (sin salida de estado)
      -C <macs>  : fusionar los AP dados en uno virtual
      -l <archivo>: escribir clave en archivo. Sobrescribe el archivo.

  Opciones de crackeo estático de WEP:

      -c         : buscar solo caracteres alfanuméricos
      -t         : buscar solo caracteres decimales codificados binarios
      -h         : buscar la clave numérica para Fritz!BOX
      -d <máscara>: usar enmascaramiento de la clave (A1:XX:CF:YY)
      -m <maddr> : dirección MAC para filtrar paquetes utilizables
      -n <nbits> : longitud de la clave WEP: 64/128/152/256/512
      -i <índice> : índice de clave WEP (1 a 4), por defecto: cualquiera
      -f <fudge> : factor de fudge para fuerza bruta, por defecto: 2
      -k <korek> : deshabilitar un método de ataque (1 a 17)
      -x o -x0  : deshabilitar fuerza bruta para los últimos bytes de clave
      -x1        : fuerza bruta para el último byte de clave (por defecto)
      -x2        : habilitar fuerza bruta para los últimos 2 bytes de clave
      -X         : deshabilitar fuerza bruta con múltiples hilos
      -y         : modo de fuerza bruta experimental único
      -K         : utilizar solo ataques antiguos de KoreK (pre-PTW)
      -s         : mostrar la clave en ASCII durante el crackeo
      -M <num>   : especificar número máximo de IVs a utilizar
      -D         : WEP decloak, omite secuencias de teclas rotas
      -P <num>   : depuración PTW: 1: deshabilitar Klein, 2: PTW
      -1         : ejecutar solo 1 intento para crackear la clave con PTW
      -V         : ejecutar en modo de inspección visual

  Opciones de crackeo de WEP y WPA-PSK:

      -w <palabras> : ruta a archivo(s) de lista(s) de palabras
      -N <archivo>  : ruta a nombre de sesión nuevo
      -R <archivo>  : ruta a nombre de sesión existente

  Opciones de WPA-PSK:

      -E <archivo>  : crear archivo de proyecto EWSA v3
      -I <cadena>   : cadena PMKID (hashcat -m 16800)
      -j <archivo>  : crear archivo Hashcat v3.6+ (HCCAPX)
      -J <archivo>  : crear archivo Hashcat (HCCAP)
      -S            : prueba de velocidad de crackeo de WPA
      -Z <seg>      : longitud de ejecución de prueba de velocidad de crackeo de WPA
      -r <DB>       : ruta a base de datos airolib-ng (no se puede usar con -w)

  Selección SIMD:

      --lista-simd       : Mostrar una lista de las arquitecturas SIMD disponibles para esta máquina.
      --simd=<opción>    : Usar una arquitectura SIMD específica.

      <opción> puede ser una de las siguientes, dependiendo de tu plataforma:

                   genérica
                   avx512
                   avx2
                   avx
                   sse2
                   altivec
                   power8
                   asimd
                   neon

  Otras opciones:

      -u         : Muestra # de CPUs y soporte SIMD
      --help    : Muestra esta pantalla de uso
```

Espero que esto sea útil para entender cómo utilizar las diferentes opciones y comandos disponibles en `aircrack-ng`.
