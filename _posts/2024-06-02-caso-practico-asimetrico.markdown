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



## Referencias

- [https://elibro.net/es/lc/uniminuto/titulos/41843][2]
- [https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos][3]
- [https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html][5]
- [https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/][5]
  
[1]: https://www.bearssl.org/tls13.html

