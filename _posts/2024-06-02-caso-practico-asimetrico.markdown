---
layout: post
title:  "Caso practico de criptografía asimétrica"
date:   2024-06-02 20:10:05 +0530
categories: RSA
---
En la actualidad se utiliza algo llamado relleno en criptografía RSA, esto es necesario entre otras cosas debido a que en algunas ocasiones la estructura de los mensajes pueden dar una luz sobre el contenido del mensaje. Rellenar un mensaje implica agregar datos aleatorios al mensaje para eliminar las pistas causadas por el formato original del mismo.

- RSA-OAEP (Optimal Asymetric Encryption Padding) o su versión modificada RSA-OAEP+. Este tipo de relleno es usado por ejemplo en PKCS#1 y en la red de anonimato TOR
- RSA-SAEP+ (Simplified Asymmetric Encryption Padding)
- RSA-REACT
- RSA-PSS (Probabilistic Signature Scheme). Usado por ejemplo en PKCS#1

Una aplicación práctica de RSA con relleno PSS es el protocolo de seguridad TLS (Transport Layer Security) o Protocolo SSL 3.0. Este fue diseñado para facilitar la privacidad y la seguridad de los datos en las comunicaciones por Internet. TLS encripta las comunicaciones entre aplicaciones web y servidores. TLS también puede usarse para encriptar otras comunicaciones como el correo electrónico, los mensajes y la voz sobre IP (VoIP).

El protocolo TLS se ubica entre la capa de aplicación y la capa TCP.


![Imagen1](/assets/protocoloTLS.JPG)

TLS utiliza algo llamado conjunto de cifrado que es un grupo de algoritmos que se utilizan para establecer una conexión de comunicaciones segura. Acordar qué conjunto de cifrado se utilizará es una parte importante del protocolo de enlace TLS. Estos algoritmos se usan en el proceso de negociación de parámetros y generación de claves que se realiza durante el handshake y cada uno tiene una finalidad específica.

Un ejemplo de un conjunto de cifrado es:

![Imagen2](/assets/Conjuntodecifrado.JPG)

Donde SSL es el protocolo, DH es el algoritmo de intercambio de clave asimétrico (Key Exchange), RSA es el método de autentificación durante el handshake, DES es el de cifrado simétrico, CBC su modo de operación y SHA el de hashing.

El subprotocolo Handshake es el que negocia una clave simétrica que se utilizará para autentificar los mensajes y cifrarlos. Para esto, el protocolo usa criptografía asimétrica para realizar un intercambio de clave (Key Exchange) generando una clave preliminar de 48 bytes denominada pre_master_secret. Se pueden usar tres algoritmos para intercambiar esta clave: RSA, Diffie-Hellman (DH), y FORTEZZA. 

Cuando el método de intercambio de claves es RSA, el Cliente genera una pre_master_secret y la cifra con la clave pública del Servidor. Ella puede ser fija y surgida de su certificado enviado previamente al Cliente, o efímera, generada para la conexión en particular. El Servidor recibe la clave simétrica preliminar y la descifra con su clave privada. 

Cuando el método de intercambio de claves es Diffie-Hellman Efímero (DHE), tanto cliente como servidor generan sus parámetros en cada negociación y los envía al otro extremo en un mensaje del handshake. En esta modalidad los parámetros no surgen de un certificado por lo que su autentificación se realiza con firmas digitales utilizando la clave privada del certificado habilitada para la firma en modalidad RSA o DSS (Digital Signature Standard).


## Referencias

- [https://www.bearssl.org/tls13.html][1]
- [http://bibliotecadigital.econ.uba.ar/download/tpos/1502-2213_QuirogaC.pdf][2]

[1]: https://www.bearssl.org/tls13.html
[2]: http://bibliotecadigital.econ.uba.ar/download/tpos/1502-2213_QuirogaC.pdf

