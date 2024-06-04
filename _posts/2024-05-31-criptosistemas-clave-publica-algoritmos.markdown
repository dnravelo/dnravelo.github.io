---
layout: post
title:  "Algoritmos para criptosistemas de clave pública"
date:   2024-05-31 22:10:05 +0530
categories: Criptosistemas Seguridad
---

## Algoritmos principalmente usados en criptosistemas de clave pública
Algunos de los algoritmos representativos de la criptografía de clave pública son:
- **RSA**: Es uno de los primeros sistemas de este tipo y se utiliza ampliamente para la seguridad de datos. Se basa en la dificultad de factorizar grandes números compuestos.
- **Criptografía de curva elíptica (ECC)**: Proporciona seguridad comparable a RSA pero con claves más cortas, lo que la hace más eficiente.
- **Diffie-Hellman**: Este es un método específico para intercambiar claves criptográficas de manera segura a través de un canal público.


## RSA
Fué desarrollado en 1977 por investigadores del MIT y se usa ampliamente tanto para cifrar como para firmar digitalmente. Usa números primos muy grandes para realizar las operaciones de cifrado. Funciona teniendo en cuenta que el algoritmo es fácil de calcular en una dirección pero muy difícil en el sentido ya que utiliza funciones trampa que cumplen esta premisa. 

Ejemplo: Si decimos que 303557 es el resultado de multiplicar dos números primos, encontrar dichos números es un trabajo con cierto nivel de dificultad, pero si hablamos de buscar el resutlado de multiplicar 757*401, la dificultad baja considerablemente, mas aún si hablamos de numeros muy grandes.

Entonces, la segurdad de RSA radica en la dificultad de factorizar un numero grande, en los números primos que lo comoponen, teniendo en cuenta que el tamaño de los números primos usados en RSA varía entre 512 bits (155 dígitos) y 2048 bits (617 dígitos)

Sin embargo se debe tener en cuenta que se han realizado avances y hoy existen algoritmos que presentan cierto nivel de eficiencia para factorizar números grandes, como el Tamiz de campo numérico general, además la eficiencia computacional crece a un ritmo muy rápido. Por lo anterior se ha venido aumentando el tamaño de las claves en RSA con el fin de mantenerlo al día y esto ha generado que se aumenten los tiempos de cifrado y descifrado.

## ECC
Se basa en matemáticas avanzadas, específicamente las curvas elípticas. La ecuación de una curva elíptica es la siguiente, donde donde \(a\) y \(b\) son constantes y la curva se define sobre un campo finito

$$
y^2=x^3 + ax + b
$$

![Image](/assets/curvaeliptic.JPG){: .center-image }*(°0°)*


Estas curvas son horizontalmente simetricas y cualquier línea recta no vertical dibujada a través de una curva elíptica siempre intersecará la curva en, como máximo, tres lugares. La seguridad de la criptografía de curva elíptica se basa en la dificultad de resolver lo que se conoce como el problema de logaritmo discreto de la curva elíptica. Dado un punto P en la curva y un escalar k, es extraordinariamente difícil determinar el punto Q de modo que Q = k*P

La ventajas de esta criptografía es que usa menor tamaño en las claves por lo que requiere menos recursos computacionales y menos ancho de banda para generar, cifrar y descifrar claves y es por esta razón por la que es usada en dispositivos móbiles y en IoT
https://web.archive.org/web/20070127130201/http://theory.lcs.mit.edu/~rivest/rsapaper.pdf
https://eprint.iacr.org/2013/635.pdf
