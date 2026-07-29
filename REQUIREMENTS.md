# Medical Card Formatter Pro

# REQUIREMENTS.md

## Requisitos funcionales del complemento


---

# 1. Objetivo principal


Crear un complemento nativo para Anki 25.09 que permita mejorar la creación y edición de tarjetas médicas.


El complemento debe:

- automatizar formato.
- organizar información.
- facilitar edición.
- mejorar presentación.


Sin modificar nunca el contenido médico original.


---

# 2. Campos compatibles


El complemento trabajará únicamente con notas que tengan:


## Campos obligatorios


- Question
- Multiple Choice
- Correct Answer
- Extra


Si la nota no contiene estos campos:

No aplicar modificaciones.


---

# 3. Formateo automático


## 3.1 Campo Question


Aplicar:


- alineación centrada.
- limpieza HTML.
- conservación de imágenes.
- conservación de fórmulas.
- conservación de MathJax.
- conservación de LaTeX.
- conservación de negritas.
- conservación de subrayado.


No modificar texto.


Ejemplo:


Entrada:

Texto de pregunta


Salida:

Texto de pregunta centrado



---

# 3.2 Campo Multiple Choice


Debe reconocer diferentes formatos.


Ejemplos:


Formato A:


A. Opción uno

B. Opción dos

C. Opción tres



Formato B:


• Opción uno

• Opción dos

• Opción tres



Formato C:


1. Opción uno

2. Opción dos

3. Opción tres



Convertir solamente la estructura a HTML limpio.


Resultado:


<ul>

<li>Opción uno</li>

<li>Opción dos</li>

<li>Opción tres</li>

</ul>


No cambiar palabras.


No corregir opciones.


No agregar opciones.


---

# 3.3 Campo Correct Answer


Debe conservar exactamente el contenido.


Debe comprobar:


- Que existe respuesta.
- Que coincide con alguna opción.


Si detecta problema:

Mostrar advertencia.


Nunca corregir automáticamente.


---

# 3.4 Campo Extra


Aplicar:


- texto justificado.
- limpieza HTML.
- conservación de tablas.
- conservación de imágenes.
- conservación de fórmulas.
- conservación de enlaces.


No modificar contenido.


---

# 4. Principio de seguridad médica


El complemento nunca debe:


- resumir.
- interpretar.
- completar.
- corregir.
- traducir.
- cambiar información médica.


El usuario siempre debe aprobar cambios importantes.
