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
