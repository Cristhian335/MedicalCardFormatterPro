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
---

# 6. Arquitectura modular del complemento


El proyecto debe estar organizado por módulos independientes.


Estructura esperada:


MedicalCardFormatterPro/

├── __init__.py

├── config.py

├── formatter.py

├── html_cleaner.py

├── smart_paste.py

├── table_editor.py

├── backup.py

├── audit.py

├── gui.py

├── utils.py

└── logger.py



---

# 7. Responsabilidad de cada módulo


## __init__.py

Punto de entrada del add-on.

Responsable de:

- iniciar el complemento.
- registrar hooks.
- cargar configuración.
- inicializar componentes.



## config.py

Responsable de:

- preferencias del usuario.
- opciones activadas/desactivadas.
- almacenamiento mediante addonManager.



## formatter.py

Responsable de:

- formato automático de campos.
- alineación.
- listas HTML.
- organización visual.



Campos principales:

- Question.
- Multiple Choice.
- Correct Answer.
- Extra.



## html_cleaner.py

Responsable de limpiar HTML innecesario.


Debe eliminar:

- estilos basura de Word.
- estilos basura de PDF.
- spans innecesarios.
- fuentes incrustadas.
- tamaños forzados.


Debe conservar:

- imágenes.
- tablas.
- MathJax.
- LaTeX.
- enlaces.
- negritas.



## smart_paste.py

Responsable de analizar texto pegado.


Debe detectar:

- preguntas.
- opciones.
- respuestas.
- explicaciones.


Debe separar automáticamente:

Question

Multiple Choice

Correct Answer

Extra


Antes de aplicar cambios debe mostrar una vista previa.



## table_editor.py

Responsable de:

- insertar tablas.
- editar tablas.
- agregar filas.
- eliminar filas.
- agregar columnas.
- eliminar columnas.
- combinar celdas.



## backup.py

Responsable de:

- crear copias antes de modificar.
- restaurar versiones anteriores.



## audit.py

Responsable de registrar:


Ejemplo:


✓ Question centrado

✓ Extra justificado

✓ Opciones convertidas a lista

✓ No se modificó contenido médico



## gui.py

Responsable de:

- menús.
- botones.
- ventanas.
- herramientas del editor.



## utils.py

Funciones auxiliares generales.



## logger.py

Registro de:

- errores.
- advertencias.
- acciones realizadas.



---

# 8. Flujo de trabajo


Usuario edita una tarjeta.

↓

Medical Card Formatter analiza estructura.

↓

Detecta posibles mejoras de formato.

↓

Muestra vista previa.

↓

Usuario acepta.

↓

Aplica cambios.

↓

Guarda auditoría.



---

# 9. Sistema de seguridad


Antes de cambios importantes:


Crear copia temporal.


Toda modificación debe ser reversible.



---

# 10. Desarrollo por versiones


## v0.1.0

Base del complemento.

- Menú dentro de Anki.
- Configuración inicial.
- Primer formateador.


## v0.2.0

Smart Paste.

- Detección de estructura.
- Separación de campos.


## v0.3.0

Editor de tablas.

- Inserción.
- Edición.
- Conversión texto-tabla.


## v0.4.0

Herramientas avanzadas.

- Auditoría.
- Backup.
- Procesamiento múltiple.



---

# 11. Objetivo final


Crear un complemento profesional para Anki que permita crear tarjetas médicas más rápido, manteniendo siempre:

- exactitud del contenido.
- seguridad.
- compatibilidad.
- facilidad de uso.


Medical Card Formatter Pro debe mejorar Anki, nunca reemplazarlo.
