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
