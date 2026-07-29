# Medical Card Formatter Pro

# DEVELOPMENT_PLAN.md

## Plan de desarrollo del complemento


---

# Filosofía de desarrollo


El proyecto debe desarrollarse por fases.

Cada fase debe producir una versión funcional e instalable.

No avanzar a la siguiente fase si la anterior no funciona correctamente.


Cada versión debe incluir:

- código funcional.
- documentación actualizada.
- CHANGELOG actualizado.
- PROJECT_STATUS actualizado.
- archivo instalable .ankiaddon.


---

# FASE 0 — Preparación del proyecto

## Objetivo

Crear la estructura inicial del complemento.


Tareas:


- Crear estructura de carpetas.
- Crear punto de entrada del add-on.
- Crear configuración inicial.
- Crear sistema básico de logging.
- Crear README técnico.


Resultado esperado:


Complemento reconocido por Anki.



Versión:

v0.0.1



---

# FASE 1 — Complemento base funcional


## Objetivo


Crear la primera versión instalable.


Funciones:


- Registrar menú dentro de Anki.
- Crear ventana básica.
- Crear configuración inicial.
- Detectar notas compatibles.


Menú:


Herramientas

↓

Medical Card Formatter Pro



Resultado esperado:


El usuario puede instalar el complemento y abrirlo desde Anki.


Versión:

v0.1.0



---

# FASE 2 — Formateador básico


## Objetivo


Implementar formato automático.


Funciones:


Campo Question:

- Centrar texto.


Campo Multiple Choice:

- Detectar opciones.
- Convertir listas.
- Limpiar espacios.


Campo Extra:

- Justificar texto.



Reglas:


No modificar contenido.



Resultado esperado:


Las tarjetas se formatean automáticamente.


Versión:

v0.2.0



---

# FASE 3 — Limpieza HTML


## Objetivo


Eliminar formato innecesario.


Funciones:


Eliminar:

- HTML basura.
- estilos de Word.
- estilos de PDF.
- etiquetas innecesarias.


Mantener:

- imágenes.
- tablas.
- fórmulas.
- enlaces.



Resultado esperado:


Texto limpio sin pérdida de información.


Versión:

v0.3.0
---

# FASE 4 — Smart Paste


## Objetivo


Separar automáticamente preguntas completas en los campos de Anki.



Funciones:


- Detectar pregunta.
- Detectar opciones.
- Detectar respuesta.
- Detectar explicación.



Campos generados:


Question

Multiple Choice

Correct Answer

Extra



Debe incluir:


- Vista previa antes de aplicar.
- Confirmación del usuario.
- Cancelar operación.



Regla principal:


Nunca modificar contenido.



Resultado esperado:


El usuario puede copiar una pregunta completa y convertirla en tarjeta rápidamente.


Versión:

v0.4.0



---

# FASE 5 — Editor de tablas


## Objetivo


Crear tablas editables dentro del campo Extra.



Funciones:


- Insertar tabla.
- Elegir filas.
- Elegir columnas.
- Editar celdas.
- Agregar filas.
- Eliminar filas.
- Agregar columnas.
- Eliminar columnas.
- Combinar celdas.



Compatibilidad:


- HTML.
- Anki Editor.
- AnkiDroid.
- AnkiMobile.



Resultado esperado:


Crear tablas médicas editables sin usar imágenes.



Versión:

v0.5.0



---

# FASE 6 — Sistema de seguridad


## Objetivo


Garantizar que ninguna información sea perdida.



Funciones:


- Backup automático.
- Restauración.
- Historial de cambios.
- Cancelar cambios.



Antes de modificar:


Crear copia temporal.



Resultado esperado:


Toda acción importante puede revertirse.



Versión:

v0.6.0



---

# FASE 7 — Sistema de auditoría


## Objetivo


Mostrar claramente qué hizo el complemento.



Ejemplo:


Medical Card Formatter Pro


✓ Question centrado

✓ Extra justificado

✓ Opciones organizadas

✓ No se modificó contenido médico



Funciones:


- Registro interno.
- Historial.
- Reporte de acciones.



Versión:

v0.7.0



---

# FASE 8 — Procesamiento masivo


## Objetivo


Permitir trabajar con muchas tarjetas.



Funciones:


- Seleccionar varias notas.
- Crear backup.
- Aplicar formato.
- Mostrar resumen final.



Debe pedir confirmación antes de ejecutar.



Versión:

v0.8.0



---

# FASE 9 — Optimización


## Objetivo


Preparar versión estable.



Comprobar:


- Velocidad.
- Uso de memoria.
- Compatibilidad.
- Manejo de errores.
- Instalación limpia.



Crear:


- Manual de usuario.
- Documentación final.
- Guía de solución de problemas.



Versión:

v0.9.0



---

# FASE 10 — Primera versión estable


## Objetivo


Publicar versión completa.



Debe incluir:


✓ Instalador .ankiaddon

✓ Archivo ZIP

✓ README

✓ CHANGELOG

✓ Documentación

✓ Configuración

✓ Pruebas



Versión:

v1.0.0



---

# PROCESO DE ENTREGA DE CADA VERSIÓN


Cada fase debe terminar con:



1. Código completo.

2. Pruebas realizadas.

3. Actualización de PROJECT_STATUS.md.

4. Actualización de CHANGELOG.md.

5. Creación de versión Git.

6. Generación de archivo:


MedicalCardFormatterPro_vX.X.X.ankiaddon


MedicalCardFormatterPro_vX.X.X.zip



---

# CONTROL DE VERSIONES


Formato:


v0.1.0

Primera versión funcional.


v0.2.0

Nueva funcionalidad.


v0.2.1

Corrección de errores.



No eliminar historial anterior.



---

# CONTINUIDAD DEL PROYECTO


Si el desarrollo continúa desde otra cuenta o sesión:


Primero leer:


- PROMPT_MASTER.md
- PROJECT_STATUS.md
- CHANGELOG.md
- DEVELOPMENT_PLAN.md



Nunca reiniciar el proyecto desde cero.



Continuar desde la última versión estable.



---

# REGLA FINAL


Medical Card Formatter Pro debe ser siempre:


- Un complemento nativo de Anki.
- Rápido.
- Seguro.
- Fácil de usar.
- Compatible con el flujo actual del usuario.


El objetivo no es reemplazar Anki.

El objetivo es mejorar Anki.
