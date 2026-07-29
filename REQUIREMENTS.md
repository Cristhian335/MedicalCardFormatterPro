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
---

# 5. Smart Paste


## Objetivo

Permitir al usuario copiar una pregunta completa desde cualquier fuente y separarla automáticamente en los campos de Anki.


Debe funcionar con textos provenientes de:

- ChatGPT.
- Word.
- PDF.
- páginas web.
- apuntes personales.



## Ejemplo de entrada


¿Cuál es el tratamiento inicial de la hipertensión?


A. Enalapril

B. Losartán

C. Amlodipino


Respuesta correcta:

B


Explicación:

Los antagonistas del receptor de angiotensina...



## Resultado esperado


Question:

¿Cuál es el tratamiento inicial de la hipertensión?



Multiple Choice:

A. Enalapril

B. Losartán

C. Amlodipino



Correct Answer:

B



Extra:

Los antagonistas del receptor de angiotensina...



---

# Reglas de Smart Paste


Debe:

- detectar estructura.
- separar campos.
- mostrar vista previa.


No debe:

- corregir contenido.
- completar información.
- cambiar palabras.



El usuario debe aprobar antes de guardar.



---

# 6. Editor de tablas


## Objetivo


Permitir crear tablas editables directamente dentro del campo Extra.



Debe incluir:


- Insertar tabla.
- Seleccionar número de filas.
- Seleccionar número de columnas.
- Editar celdas.
- Añadir filas.
- Eliminar filas.
- Añadir columnas.
- Eliminar columnas.
- Combinar celdas.



Las tablas deben ser HTML editable.



---

# 7. Conversión texto a tabla


Detectar formatos como:


Fármaco | Mecanismo | Uso

Enalapril | IECA | HTA

Losartán | ARA II | HTA



Convertir a:


Tabla HTML editable.



No modificar datos.



---

# 8. Limpieza HTML


Crear herramienta:


Limpiar formato



Debe eliminar:


- estilos innecesarios.
- etiquetas span innecesarias.
- fuentes incrustadas.
- tamaños forzados.
- formato basura de Word.
- formato basura de PDF.



Debe conservar:


- imágenes.
- tablas.
- listas.
- MathJax.
- LaTeX.
- enlaces.
- negritas.



---

# 9. Sistema de Backup


Antes de modificaciones:


Crear copia temporal.


Debe permitir:


- restaurar versión anterior.
- cancelar cambios.
- recuperar información.



No realizar cambios irreversibles.



---

# 10. Sistema de auditoría


Registrar acciones realizadas.


Ejemplo:


Medical Card Formatter Pro


✓ Question centrado

✓ Extra justificado

✓ Multiple Choice convertido a lista

✓ No se modificó contenido médico

✓ No se agregó información



Guardar registro de acciones.



---

# 11. Configuración del complemento


Crear menú:


Herramientas

↓

Medical Card Formatter Pro



Opciones:


- Activar/desactivar complemento.
- Activar/desactivar Smart Paste.
- Activar/desactivar limpieza HTML.
- Activar/desactivar formato automático.
- Configurar alineación.
- Configurar tablas.



Guardar configuración mediante addonManager.



---

# 12. Procesamiento múltiple


Permitir seleccionar varias notas.


Acciones:


- Formatear notas seleccionadas.
- Crear backup.
- Mostrar resumen final.



Antes de ejecutar:

Solicitar confirmación.



---

# 13. Interfaz de usuario


Debe integrarse naturalmente en Anki.


Agregar:


Menú:

Herramientas → Medical Card Formatter Pro



Botones:


- Formatear nota.
- Smart Paste.
- Insertar tabla.
- Limpiar formato.
- Restaurar versión.



La interfaz debe ser simple y rápida.



---

# 14. Requisitos de rendimiento


El complemento debe:


- iniciar rápidamente.
- no bloquear Anki.
- trabajar con colecciones grandes.
- manejar errores correctamente.



---

# 15. Pruebas necesarias


Antes de cada versión:


Comprobar:


- Instalación correcta.
- Compatibilidad con Anki 25.09.
- No romper otros complementos.
- No modificar contenido médico.
- Backup funciona.
- Restauración funciona.
- Smart Paste funciona.
- Tablas funcionan.



---

# 16. Criterio de aceptación final


El complemento será aceptado cuando:


✓ Sea instalable como .ankiaddon.

✓ Funcione dentro de Anki 25.09.

✓ Mantenga intacto el contenido médico.

✓ Mejore el formato automáticamente.

✓ Sea compatible con la plantilla actual.

✓ Sea rápido y estable.

✓ Todas las acciones sean reversibles.
