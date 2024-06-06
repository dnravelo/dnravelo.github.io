---
layout: post
title:  "Caso practico de criptografía asimétrica"
date:   2024-06-02 20:10:05 +0530
categories: RSA
---
En la actualidad se utiliza algo llamado relleno en criptografía RSA, esto es necesario entre otras cosas debido a que en algunas ocaciones la estructura de los mensajes pueden dar una luz sobre el contendio del mensaje. Rellenar un mensaje implica agregar datos aleatorios al mensaje para eliminar las pistas causadas por el formato original del mismo.

- RSA-OAEP (Optimal Asymetric Encryption Padding) o su versión moficada RSA-OAEP+. Este tipo de relleno es usado por ejemplo en PKCS#1 y en la red de anonimato TOR
- RSA-SAEP+ (Simplified Asymmetric Encryption Padding)
- RSA-REACT
- RSA-PSS (Probabilistic Signature Scheme). Usado por ejemplo en PKCS#1

Una aplicación práctica de RSA con relleno PSS es el protocolo de seguridad TLS (Transport Layer Security) diseñado para facilitar la privacidad y la seguridad de los datos en las comunicaciones por Internet. TLS encripta las comunicaciones entre aplicaciones web y servidores. TLS también puede usarse para encriptar otras comunicaciones como el correo electrónico, los mensajes y la voz sobre IP (VoIP). 

¿Qué ocurre durante un protocolo de enlace TLS?
Durante el transcurso de un protocolo de enlace TLS, el cliente y el servidor harán juntos lo siguiente:

Especificar qué versión de TLS (TLS 1.0, 1.2, 1.3, etc.) van a utilizar.
Decidir qué conjuntos de cifrado (ver más abajo) van a utilizar.
Autenticar la identidad del servidor mediante la clave pública del servidor y la firma digital de la autoridad de certificación SSL.
Generar claves de sesión para poder utilizar el cifrado simétrico una vez finalizado el protocolo de enlace.
¿Qué es un conjunto de cifrado?
Un conjunto de cifrado es un grupo de algoritmos que se utilizan para establecer una conexión de comunicaciones segura. Hay una serie de conjuntos de cifrado de amplio uso, y una parte esencial del protocolo de enlace TLS es acordar qué conjunto de cifrado se utilizará para este protocolo.
## Referencias

- [https://elibro.net/es/lc/uniminuto/titulos/41843][2]
- [https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos][3]
- [https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html][5]
- [https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/][5]
  
[1]: https://www.bearssl.org/tls13.html

