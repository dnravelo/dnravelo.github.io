---
layout: post
title:  "Criptosistemas de clave pública y su aplicación,"
date:   2024-03-06 22:10:05 +0530
categories: Criptosistemas Seguridad
---

## ¿Qué es el criptosistema de clave pública?

Un criptosistema de clave pública, también conocido como criptografía asimétrica, emplea un par de claves: una clave pública que se utiliza para el cifrado y puede ser compartida libremente y una clave privada que se utiliza para el descifrado y debe mantenerse en secreto. En este caso cuando un usuario quiere enviar un mensaje, cifra el mensaje utilizando la clave pública del receptor y cuando el receptor recibe el mensaje, lo descifra utilizando su clave privada. 

![Image](/assets/c9-img-blog-asimetrico.png)

Este tipo de encripción suele usar operaciónes matemáticas relacionadas con problemas difíciles de resolver.

En primera instancia podemos afirmar que un criptosistema de clave pública brinda confidencialidad ya que el mensaje no puede ser decifrado por un tercero e integridad ya que el mensaje no puede ser modificado durante su transmisión. 
- Mensaje + clave pública = Mensaje cifrado
- Mensaje encriptado + clave privada = Mensaje descifrado

Pero al ir mas allá, observamos que adicionalmente este criptosistema brinda autenticidad para garantizar la identidad del autor de la información y no repudio para que el emisor no puede negar haber enviado el mensajeque. Esto ocurre porque ofrece un método para el desarrollo de firmas digitales. En la firma digital se cifra el mensaje con la clave privada y solo la clave pública asociada lo puede descifrar por lo que si con la clave publica obtuvimos el mensaje original, se puede afirmar que el emisor es el correcto.
Mensaje + clave privada = Mensaje firmado
Mensaje firmado + clave pública = Autenticación

Algunos de los algoritmos representativos de los criptosistemas de clave pública incluyen Diffie-Hellman, ElGamal, RSA (Rivest-Shamir-Adleman) y ECC (Elliptic Curve Cryptography).



