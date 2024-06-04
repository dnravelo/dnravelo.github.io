---
layout: post
title:  "Criptosistemas simétricos vs Criptosistemas asimétricos"
date:   2024-06-01 20:10:05 +0530
categories: Criptosistemas Simétrico Asimétrico
---



| **Criptosistema** | **Ventanas** | **Desventajas** |
|-------|--------|---------|
| **Simétrico** | - **Rapidez**: Los algoritmos simétricos son más rápidos porque realizan operaciones menos complejas en los datos. Esto los hace ideales para cifrar grandes volúmenes de datos. <br/> - **Eficiencia** : Los sistemas simétricos son más eficientes en términos de uso de recursos computacionales. Esto es especialmente útil en dispositivos con recursos limitados.  | - **Distribución de la clave**: La necesidad de compartir una clave secreta entre las partes puede ser un desafío, especialmente en redes grandes. Si la clave se ve comprometida durante la transmisión, los datos cifrados también pueden verse comprometidos <br/> - **Gestión de claves**: En una red grande, la gestión de todas las claves simétricas puede ser complicada. |
| **Asimétrico** | - **Seguridad**: Dado que las claves privadas nunca se transmiten o comparten, hay menos riesgo de que sean interceptadas por un tercero. <br/> - **Autenticación y no repudio**: Los sistemas asimétricos permiten la autenticación de los usuarios y garantizan que un emisor no pueda negar haber enviado un mensaje. Esto es posible gracias a las firmas digitales. | - **Velocidad**: Los sistemas asimétricos son más lentos y requieren más recursos computacionales que los sistemas simétricos. Esto se debe a que los algoritmos asimétricos realizan operaciones matemáticas más complejas. <br/> - **Tamaño de la clave**: Para proporcionar el mismo nivel de seguridad, las claves en un sistema asimétrico necesitan ser significativamente más largas que en un sistema simétrico. |




## Referencias

- [https://elibro.net/es/lc/uniminuto/titulos/41843][2]
- [https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos][3]
- [https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html][5]
- [https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/][5]
  
[2]: https://elibro.net/es/lc/uniminuto/titulos/41843
[3]: https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos
[4]: https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html
[5]: https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/
