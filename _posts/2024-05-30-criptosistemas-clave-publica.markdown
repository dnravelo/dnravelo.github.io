---
layout: post
title:  "Criptosistemas de clave pública y su aplicación,"
date:   2024-05-30 22:10:05 +0530
categories: Criptosistemas Seguridad
---

## ¿Qué es el criptosistema de clave pública?

Un criptosistema de clave pública, también conocido como criptografía asimétrica, emplea un par de claves: una clave pública que se utiliza para el cifrado y puede ser compartida libremente y una clave privada que se utiliza para el descifrado y debe mantenerse en secreto. En este caso cuando un usuario quiere enviar un mensaje, cifra el mensaje utilizando la clave pública del receptor y cuando el receptor recibe el mensaje, lo descifra utilizando su clave privada.

![Image](/assets/c9-img-blog-asimetrico.png)

Este tipo de encriptación suele usar operaciones matemáticas relacionadas con problemas difíciles de resolver.

En primera instancia podemos afirmar que un criptosistema de clave pública brinda confidencialidad ya que el mensaje no puede ser descifrado por un tercero e integridad ya que el mensaje no puede ser modificado durante su transmisión.
- Mensaje + clave pública = Mensaje cifrado
- Mensaje encriptado + clave privada = Mensaje descifrado

Pero al ir más allá, observamos que adicionalmente este criptosistema brinda autenticidad para garantizar la identidad del autor de la información y no repudio para que el emisor no puede negar haber enviado el mensaje. Esto ocurre porque ofrece un método para el desarrollo de firmas digitales. En la firma digital se cifra el mensaje con la clave privada y solo la clave pública asociada lo puede descifrar por lo que si con la clave publica obtuvimos el mensaje original, se puede afirmar que el emisor es el correcto.
- Mensaje + clave privada = Mensaje firmado
- Mensaje firmado + clave pública = Autenticación

Algunos de los algoritmos representativos de los criptosistemas de clave pública incluyen Diffie-Hellman, ElGamal, RSA (Rivest-Shamir-Adleman) y ECC (Elliptic Curve Cryptography). Este tipo de encriptación suele usar problemas matemáticos de difícil solución, por ejemplo, el algoritmo RSA usa el problema de la factorización de números grandes, mientras que los algoritmos Diffie-Hellman y ECC usan el problema del logaritmo discreto



## Referencias

- [https://elibro.net/es/lc/uniminuto/titulos/106503][1]
- [https://elibro.net/es/lc/uniminuto/titulos/41843][2]
- [https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos][3]
- [https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html][5]
- [https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/][5]
  
[1]: https://elibro.net/es/lc/uniminuto/titulos/106503
[2]: https://elibro.net/es/lc/uniminuto/titulos/41843
[3]: https://www.researchgate.net/publication/28106424_Introduccion_a_la_Criptografia_tipos_de_algoritmos
[4]: https://mikelgarcialarragan.blogspot.com/2016/07/criptografia-xxi-criptologia-para-todos.html
[5]: https://www.keepersecurity.com/blog/es/2023/06/07/what-is-elliptic-curve-cryptography/
