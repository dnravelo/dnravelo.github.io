---
layout: post
title:  "Criptografía y Criptosistemas"
date:   2024-05-27 19:03:36 +0530
categories: Criptografia NodeJS
---
## ¿Qué es la criptografía?

La criptografía es la ciencia y el arte de proteger la información mediante la transformación de datos legibles en datos codificados, de manera que solo las personas autorizadas puedan acceder a la información original. Utiliza algoritmos matemáticos y técnicas de cifrado para garantizar características de seguridad como:
- **Confidencialidad**: garantizar que solo las personas autorizadas tienen acceso a la información.
- **Integridad**: garantizar que el documento original no ha sido modificado.
- **Autenticidad**: garantizar la identidad del autor de la información.

## ¿Qué es un criptosistema?

Un criptosistema es un conjunto de algoritmos, protocolos y procedimientos que permiten la implementación de técnicas criptográficas para proteger la información. Incluye los métodos para el cifrado y descifrado de datos, la gestión de claves y otros mecanismos de seguridad asociados. 
Los criptosistemas utilizan distintos métodos de cifrado que se dividen en cifrado de flujo y cifrado de bloque. Este último presenta dos tipos: el cifrado de clave pública y el cifrado de clave privada. 

![Image](/assets/Criptosistemas.JPG)

## ¿Qué es un criptosistema de clave privada?
Un criptosistema de clave privada, también conocido como criptografía simétrica, utiliza la misma clave para el cifrado y descifrado de la información. Esto implica que tanto el remitente como el receptor deben conocer y mantener en secreto la clave utilizada. Algunos ejemplos de algoritmos simétricos son AES (Advanced Encryption Standard) y DES (Data Encryption Standard).
En este tipo de cifrado el emisor cifra el mensaje con su clave privada, lo envía a través del canal inseguro y el destinatario lo descifra con la misma contraseña o clave privada. 
Un algoritmo de clave simétrica debe cumplir las siguientes características para que sea seguro para tener buenas características:
•	El algoritmo debe ser público y conocido cumpliendo el principio de Kerckhoffs que establece que de un sistema criptográfico debe conocerse el diseño y funcionamiento permaneciendo invulnerable. Lo único que debe permaneces secreto es la clave.
•	No se podrá obtener la clave de cifrado ni tampoco el mensaje en claro una vez se haya cifrado el mensaje.
•	El costo de obtener la clave a partir del mensaje cifrado y el mensaje debe ser mucho mayor que el valor que pueda tener la información.
•	Las claves deben ser lo más pequeñas posible para facilitar su implementación y rendimiento, pero lo suficientemente grandes para resistir ataques de fuerza bruta.
•	Las operaciones de cifrado no deben ser tan complejas que superen las capacidades de cómputo actuales.
•	Es ideal que el algoritmo no expanda el mensaje.

## Referencias

- [https://elibro.net/es/lc/uniminuto/titulos/106503][1]
- [https://elibro.net/es/lc/uniminuto/titulos/41843][2]
- [https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos][3]

[1]: https://elibro.net/es/lc/uniminuto/titulos/106503
[2]: https://elibro.net/es/lc/uniminuto/titulos/41843
[3]: https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos

