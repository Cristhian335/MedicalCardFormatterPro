# Medical Card Formatter Pro

# ARCHITECTURE.md

## Arquitectura del proyecto


## 1. Descripción general

Medical Card Formatter Pro es un complemento nativo para Anki 25.09.

No es una aplicación independiente.

Su objetivo es mejorar el flujo de creación y edición de tarjetas médicas dentro de Anki.

Debe ser:

- rápido.
- ligero.
- estable.
- modular.
- fácil de mantener.
- compatible con otros complementos.


---

# 2. Principio fundamental

El complemento nunca debe modificar el contenido médico.

Únicamente puede modificar:

- formato HTML.
- estructura visual.
- alineación.
- listas.
- tablas.
- presentación.


Nunca debe:

- resumir.
- corregir.
- completar.
- interpretar.
- agregar información.
- eliminar información.
- cambiar términos médicos.
- cambiar dosis.
- cambiar unidades.


El usuario siempre mantiene el control.


---

# 3. Compatibilidad con Anki

Versión objetivo:

Anki 25.09


Debe utilizar:

- API oficial de Anki.
- Hooks oficiales.
- Métodos recomendados.


No debe modificar:

- archivos internos de Anki.
- base de datos directamente.
- scheduler.
- sistema de repaso.
- sincronización.


---

# 4. Compatibilidad con complementos existentes

Debe coexistir con otros add-ons instalados.

No debe:

- sobrescribir funciones existentes.
- cambiar atajos actuales.
- modificar configuraciones externas.


Si existe conflicto:

- informar al usuario.
- desactivar solamente la función conflictiva.


---

# 5. Compatibilidad con plantilla actual

El usuario posee una plantilla personalizada.

La plantilla utiliza:

- HTML.
- CSS.
- JavaScript.
- sistema de checkbox.
- mezcla aleatoria de opciones.
- Persistence.


El complemento NO debe modificar estos elementos.

Debe preparar correctamente los campos:

- Question.
- Multiple Choice.
- Correct Answer.
- Extra.


El campo Multiple Choice debe continuar funcionando con el script actual.
