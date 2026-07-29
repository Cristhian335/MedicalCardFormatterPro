# Medical Card Formatter Pro

# CLAUDE_WORKFLOW.md

## Flujo de trabajo con Claude y GitHub


---

# 1. Objetivo


Este documento define cómo debe trabajar Claude durante el desarrollo del complemento.


Claude debe utilizar este repositorio como fuente principal de información.


Antes de modificar código debe leer:


- PROMPT_MASTER.md
- PROJECT_STATUS.md
- ARCHITECTURE.md
- REQUIREMENTS.md
- DEVELOPMENT_PLAN.md
- CHANGELOG.md



---

# 2. Regla principal


No comenzar desarrollo sin revisar el estado actual del proyecto.


Antes de crear código:


1. Leer documentación.

2. Revisar versión actual.

3. Revisar funciones completadas.

4. Revisar funciones pendientes.



---

# 3. Método de desarrollo


El desarrollo debe hacerse por fases.


Cada fase debe:


- tener un objetivo claro.
- generar código funcional.
- ser probada.
- actualizar documentación.
- crear una versión.



No desarrollar varias fases al mismo tiempo.



---

# 4. Inicio de una nueva sesión


Cuando Claude inicia una nueva sesión:


Debe responder primero:


"Voy a revisar el estado actual del proyecto."



Después:


Leer:

PROJECT_STATUS.md



Identificar:


- versión actual.
- último avance.
- siguiente tarea pendiente.



---

# 5. Modificación de código


Antes de cambiar archivos:


Claude debe indicar:


- qué archivo modificará.
- qué función agregará.
- qué problema resolverá.



Después debe realizar cambios.



---

# 6. Actualización obligatoria


Después de completar una tarea:


Actualizar:


## PROJECT_STATUS.md


Debe incluir:


- nueva versión.
- funciones terminadas.
- funciones pendientes.
- errores conocidos.



## CHANGELOG.md


Debe incluir:


- fecha.
- cambios realizados.
- correcciones.



---

# 7. Sistema de versiones


Formato:


v0.1.0

Nueva funcionalidad.



v0.1.1

Corrección de errores.



v0.2.0

Nueva etapa importante.



Nunca borrar versiones anteriores.
---

# 8. Solicitud de nuevas funciones


Cuando se quiera agregar una función nueva:


Primero actualizar:


REQUIREMENTS.md


Después:


DEVELOPMENT_PLAN.md


Luego comenzar programación.



No agregar funciones no documentadas.



---

# 9. Generación de código


Claude debe:


- Crear archivos completos.
- Mantener estructura modular.
- Evitar código innecesario.
- Usar nombres claros.
- Documentar funciones importantes.



No crear:


- archivos duplicados.
- código temporal sin aviso.
- cambios fuera del objetivo.



---

# 10. Pruebas antes de entregar


Antes de crear una versión:


Comprobar:


✓ El complemento inicia.

✓ Anki abre correctamente.

✓ No hay errores críticos.

✓ Las funciones nuevas funcionan.

✓ No modifica contenido médico.

✓ Mantiene compatibilidad.



---

# 11. Creación de versión instalable


Cada versión funcional debe generar:


Archivo principal:


MedicalCardFormatterPro_vX.X.X.ankiaddon



También crear:


MedicalCardFormatterPro_vX.X.X.zip



La versión debe incluir:


- código completo.
- documentación.
- archivos necesarios.



---

# 12. Uso de GitHub


Cada cambio importante debe generar un commit.


Formato recomendado:


v0.1.0 - Base del complemento creada


v0.2.0 - Formateador automático añadido


v0.3.0 - Smart Paste añadido



Los mensajes deben ser claros.



---

# 13. Creación de Releases


Cuando una versión sea estable:


Crear Release en GitHub.


Debe incluir:


- número de versión.
- descripción de cambios.
- archivo .ankiaddon.
- archivo ZIP.



Ejemplo:


Release:


Medical Card Formatter Pro v0.1.0



Archivos:


MedicalCardFormatterPro_v0.1.0.ankiaddon

MedicalCardFormatterPro_v0.1.0.zip



---

# 14. Continuar desde otra cuenta de Claude


Si se cambia de cuenta:


No explicar nuevamente todo el proyecto.


Realizar:


1. Abrir repositorio GitHub.


2. Pedir a Claude:


"Lee el repositorio completo y continúa desde el estado actual."



Claude debe revisar:


- PROJECT_STATUS.md.
- CHANGELOG.md.
- DEVELOPMENT_PLAN.md.



Después continuar desde la última tarea pendiente.



---

# 15. Si se alcanza límite de tokens


Claude debe detenerse de forma ordenada.


Antes de terminar:


Actualizar:


- PROJECT_STATUS.md.
- CHANGELOG.md.



Guardar código completo.


Crear commit.


Indicar:


- qué está terminado.
- qué falta.
- próximo paso recomendado.



---

# 16. Regla de seguridad del proyecto


Siempre recordar:


Medical Card Formatter Pro no es una inteligencia artificial médica.


No analiza contenido clínico.


No toma decisiones.


No corrige información médica.


Solamente organiza y mejora presentación dentro de Anki.



---

# 17. Estado final esperado


El proyecto debe terminar siendo:


✓ Un complemento nativo de Anki.

✓ Instalable mediante .ankiaddon.

✓ Compatible con Anki 25.09.

✓ Modular.

✓ Rápido.

✓ Seguro.

✓ Fácil de mantener.



El objetivo es mejorar la creación de tarjetas médicas sin alterar la información original del usuario.
