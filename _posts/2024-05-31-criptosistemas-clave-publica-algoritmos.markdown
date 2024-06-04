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

El tamaño de los números primos usados en RSA varía entre 512 bits (155 dígitos) y 2048 bits (617 dígitos)



https://web.archive.org/web/20070127130201/http://theory.lcs.mit.edu/~rivest/rsapaper.pdf
