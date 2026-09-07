# Alfabetización Informática (LM-105)
## Unidad I: Introducción a la Informática — Código ASCII

**Profesor:** [Tu Nombre / Gemini Notebook]  
**Asignatura:** Alfabetización Informática  
**Tema:** Código ASCII e Intercambio de Información  

---

# ¿Qué es el Código ASCII?
### "American Standard Code for Information Interchange"

* **Definición:** Es un sistema de codificación de caracteres que asigna un valor numérico único a cada letra, número, símbolo o comando.
* **El Acrónimo:** Código Estándar Estadounidense para el Intercambio de Información.
* **El Concepto Central:** Funciona como el "traductor universal" que permite a los sistemas electrónicos (que operan en binario con $0$ y $1$) procesar, almacenar y representar texto comprensible para los humanos.

---

# ¿Por qué se creó? El Problema de Incompatibilidad

* **La Torre de Babel Digital (Previa a 1963):**
  * En los inicios de la computación, cada fabricante de hardware (IBM, UNIVAC, etc.) utilizaba su propio sistema privado de códigos para representar letras y números.
  * Si un sistema intentaba enviar un archivo de texto a una computadora de otra marca, el archivo se volvía ilegible (caracteres extraños o inválidos).
* **El Nacimiento del Estándar:**
  * En la década de 1960, un comité de la *American Standards Association* (hoy **ANSI**) liderado por el pionero de la informática **Robert W. Bemer**, se propuso unificar la codificación.
  * Su objetivo era resolver los problemas de interoperabilidad, permitiendo la comunicación fluida entre redes y periféricos.

---

# ¿Cómo funciona? De Binario a Carácter

Las computadoras solo comprenden niveles de voltaje representados lógicamente por dígitos binarios o bits ($0$ y $1$). El Código ASCII es la tabla que traduce esos números:

$$\text{Tecla "A"} \longrightarrow \text{Decimal } 65 \longrightarrow \text{Binario } 01000001$$

```
+------------+-----------------+-------------+
| Carácter   | Código Decimal  | Binario     |
+------------+-----------------+-------------+
| Espacio    | 32              | 00100000    |
| '0'        | 48              | 00110000    |
| 'A'        | 65              | 01000001    |
| 'a'        | 97              | 01100001    |
+------------+-----------------+-------------+
```

* **Nota Pedagógica:** La diferencia numérica entre letras mayúsculas y minúsculas es exactamente de 32 (un bit de diferencia), facilitando las operaciones del procesador.

---

# Estructura del Código ASCII Estándar (7 Bits)

El estándar original utiliza **7 bits** para codificar la información. Esto genera exactamente $2^7 = 128$ combinaciones únicas (valores del 0 al 127), divididas en dos grandes bloques:

### 1. Caracteres de Control (0 al 31 y 127)
* **Función:** Comandos no imprimibles diseñados para dirigir el hardware (impresoras y teletipos).
* **Ejemplos:**
  * `0 (NULL)`: Fin de cadena de texto.
  * `7 (BEL)`: Emite un sonido de advertencia ("beep").
  * `8 (BS)`: Borrar un carácter hacia atrás (*Backspace*).
  * `13 (CR)`: Retorno de carro (inicio de línea).

---

# Estructura del Código ASCII Estándar (7 Bits)

### 2. Caracteres Imprimibles (32 al 126)
* **Función:** Símbolos visibles en pantalla y papel que forman el texto.
* **Composición:**
  * **Espacio (32):** El inicio del texto plano.
  * **Letras Mayúsculas (65 a 90):** De la 'A' a la 'Z'.
  * **Letras Minúsculas (97 a 122):** De la 'a' a la 'z'.
  * **Números (48 a 57):** Del '0' al '9'.
  * **Puntuación y Símbolos (33-47, 58-64, 91-96, 123-126):** Signos como `!`, `*`, `@`, `[`, `{`, etc.

---

# El ASCII Extendido (8 Bits)

A medida que la informática se expandió internacionalmente, las 128 combinaciones originales (diseñadas para el inglés) resultaron insuficientes: faltaban los acentos del español, la 'ñ', la 'ç' francesa o la diéresis alemana.

* **La Solución:** Expandir la representación de caracteres a un byte completo de **8 bits**.
* **Capacidad:** $2^8 = 256$ combinaciones posibles (valores del 0 al 255).
* **Bloque Extendido (128 al 255):**
  * Caracteres acentuados de lenguas europeas (`á`, `é`, `í`, `ó`, `ú`, `ñ`, `Ñ`).
  * Símbolos matemáticos avanzados ($\pm$, $\div$, $\approx$).
  * Caracteres de dibujo de marcos para diseñar pantallas en sistemas operativos de modo texto (como MS-DOS).

---

# ¿Por qué es tan importante en la informática?

1. **La Base del Texto Plano (.txt):** Los documentos sencillos y los archivos de configuración utilizan ASCII para garantizar que cualquier programa o sistema operativo del mundo pueda abrirlos y leerlos.
2. **Programación y Cadenas:** En lenguajes de programación como C, Java o Python, los caracteres se manipulan internamente mediante sus valores ASCII. El uso de funciones como `ord('A') -> 65` es básico para programar algoritmos de búsqueda y ordenamiento de texto.
3. **Protocolos de Internet y Web:** Los protocolos que sostienen internet, como HTTP (para páginas web) y SMTP (para correos electrónicos), transmiten sus encabezados y comandos principales usando texto ASCII estándar.
4. **Entidades HTML y URLs:** Los caracteres especiales en la web se representan a menudo mediante entidades numéricas basadas en ASCII para evitar problemas de compatibilidad en diferentes navegadores.

---

# Limitaciones y la Evolución hacia Unicode

A pesar de su inmensa importancia, el código ASCII (incluso el extendido de 8 bits) se quedó pequeño para el mundo globalizado:
* No puede representar idiomas no latinos (como el japonés, mandarín, cirílico, árabe o hebreo).
* La existencia de "tablas de caracteres locales" conflictivas provocaba que un archivo creado en una región se viera con caracteres rotos en otra.

### El Sucesor Universal: Unicode y UTF-8
* **Unicode:** Diseñado para almacenar más de 140,000 caracteres, cubriendo prácticamente todas las escrituras humanas y emojis.
* **La Herencia de ASCII:** Para garantizar la compatibilidad, la codificación universal **UTF-8** diseñó sus primeros 128 códigos de manera **idéntica al código ASCII**. Cualquier archivo de texto ASCII válido es, por definición, un archivo UTF-8 válido.

---

# Resumen para el Laboratorio

* El hardware solo procesa voltajes ($0$ y $1$).
* **ASCII** es el estándar de oro original de los años 60 que transformó esos dígitos binarios en caracteres semánticos legibles para nosotros.
* El dominio técnico de este código es indispensable para comprender cómo viaja la información por las redes, cómo se codifican las bases de datos y cómo interactúan el hardware y el software en un mismo sistema informático.
