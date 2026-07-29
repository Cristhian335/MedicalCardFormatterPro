# PROMPT PARA CLAUDE CODE

# Medical Card Formatter Pro - Anki Add-on

Actúa como un desarrollador senior especializado en creación de complementos para Anki, Python, PyQt6 y la API oficial de Anki 25.09.

Quiero que desarrolles un complemento nativo para Anki llamado:

# Medical Card Formatter Pro

IMPORTANTE:

NO crear una plataforma externa.

NO crear una aplicación independiente.

NO crear un programa separado.

Debe ser exclusivamente un ADD-ON NATIVO DE ANKI.

Debe integrarse dentro de Anki y mejorar mi flujo actual.

Debe ser ligero, rápido, estable y práctico para uso diario.

====================================================
OBJETIVO PRINCIPAL
==================

Crear un complemento para estudiantes de medicina que permita crear y mantener tarjetas médicas de alta calidad sin cambiar mi método actual de estudio.

El complemento debe:

* organizar contenido,
* mejorar formato,
* limpiar HTML,
* facilitar edición,
* insertar tablas,
* separar información,

pero NUNCA modificar el contenido médico.

====================================================
REGLA ABSOLUTA DE CONTENIDO MÉDICO
==================================

El complemento NUNCA debe:

* resumir información.
* corregir información médica.
* interpretar información.
* completar información faltante.
* inventar información.
* cambiar palabras.
* cambiar nombres de medicamentos.
* cambiar dosis.
* cambiar unidades.
* cambiar símbolos médicos.
* cambiar abreviaturas.

El contenido introducido por el usuario debe permanecer exactamente igual.

Solo puede modificar:

* formato HTML,
* alineación,
* listas,
* tablas,
* estructura visual.

====================================================
COMPATIBILIDAD
==============

Debe funcionar en:

Anki 25.09

Windows

macOS

Linux

Debe ser compatible con complementos existentes.

NO modificar:

* scheduler.
* sistema de repaso.
* sincronización.
* base de datos interna.
* templates actuales.
* CSS actual.
* JavaScript actual.

Debe usar únicamente hooks oficiales de Anki.

Debe poder desinstalarse sin dejar cambios permanentes.

====================================================
TIPO DE NOTA
============

Trabajar únicamente con este tipo de nota:

Campos:

Question

Multiple Choice

Correct Answer

Extra

No modificar otros tipos de nota.

====================================================
COMPATIBILIDAD CON MI TEMPLATE ACTUAL
=====================================

Tengo una plantilla personalizada que:

* mezcla las opciones.
* añade checkbox automáticamente.
* utiliza Persistence para recordar selecciones.

El complemento NO debe cambiar esta lógica.

Debe preparar correctamente el campo:

Multiple Choice

para que siga funcionando con mi script actual.

====================================================
FUNCIONES PRINCIPALES
=====================

# 1. FORMATEO AUTOMÁTICO AL GUARDAR

## Question

Aplicar automáticamente:

* texto centrado.
* mantener imágenes.
* mantener fórmulas.
* mantener MathJax.
* mantener LaTeX.
* mantener negritas.
* mantener colores.
* mantener subrayados.

No modificar texto.

## Multiple Choice

Detectar automáticamente opciones escritas como:

Formato 1:

A. Opción

B. Opción

C. Opción

Formato 2:

• Opción

• Opción

Formato 3:

* Opción

* Opción

Formato 4:

1. Opción

2. Opción

Convertir internamente a HTML limpio:

<ul>
<li>Opción</li>
<li>Opción</li>
</ul>

Eliminar:

* espacios vacíos innecesarios.
* saltos duplicados.

No modificar palabras.

## Correct Answer

Mantener exactamente igual.

Comprobar que la respuesta existe dentro de Multiple Choice.

Si no coincide:

mostrar advertencia.

No modificar automáticamente.

## Extra

Aplicar:

* texto justificado.
* mantener imágenes.
* mantener tablas.
* mantener listas.
* mantener fórmulas.
* mantener enlaces.

====================================================
2. SMART PASTE
==============

Crear un botón dentro del editor:

Smart Paste

Debe detectar bloques como:

Pregunta:

¿Cuál es el tratamiento inicial?

A. Enalapril

B. Losartán

C. Amlodipino

Respuesta correcta:

B

Explicación:

Texto...

Y separar automáticamente:

Question

Multiple Choice

Correct Answer

Extra

Antes de aplicar cambios:

Mostrar vista previa.

El usuario debe aceptar.

====================================================
3. EDITOR DE TABLAS
===================

Agregar botón:

Insertar tabla

Permitir:

* seleccionar filas.
* seleccionar columnas.
* editar celdas.
* agregar filas.
* eliminar filas.
* agregar columnas.
* eliminar columnas.
* combinar celdas.

Las tablas deben ser HTML editable.

====================================================
4. CONVERTIR TEXTO EN TABLA
===========================

Si encuentra:

Fármaco | Mecanismo | Uso

Enalapril | IECA | HTA

Losartán | ARA II | HTA

Convertir automáticamente a tabla HTML.

No modificar datos.

====================================================
5. LIMPIADOR HTML
=================

Crear botón:

Limpiar formato

Eliminar:

* estilos basura de Word.
* estilos basura de PDF.
* spans innecesarios.
* fuentes incrustadas.
* tamaños forzados.
* márgenes innecesarios.

Mantener:

* imágenes.
* tablas.
* listas.
* negritas.
* fórmulas.

====================================================
6. BACKUP Y RESTAURACIÓN
========================

Antes de cambios importantes:

crear copia temporal.

Permitir:

Restaurar versión anterior.

====================================================
7. MODO AUDITORÍA
=================

Después de aplicar cambios mostrar:

Medical Card Formatter Pro

✓ Question centrado

✓ Extra justificado

✓ Opciones convertidas a lista

✓ No se modificó contenido médico

✓ No se agregaron palabras

====================================================
8. CONFIGURACIÓN
================

Crear menú:

Herramientas

Medical Card Formatter Pro

Opciones:

* Activar/desactivar.
* Activar/desactivar Smart Paste.
* Activar/desactivar limpieza HTML.
* Configurar alineaciones.
* Configurar tablas.

Guardar configuración usando addonManager.

====================================================
ESTRUCTURA DEL PROYECTO
=======================

Crear proyecto modular:

MedicalCardFormatterPro/

**init**.py

config.json

formatter.py

smart_paste.py

table_editor.py

html_cleaner.py

backup.py

gui.py

utils.py

logger.py

README.md

INSTALL.md

CHANGELOG.md

PROJECT_STATUS.md

====================================================
DESARROLLO POR FASES
====================

No intentar crear todo en una sola respuesta.

FASE 1:

Crear complemento base funcional.

Debe generar:

MedicalCardFormatterPro.zip

MedicalCardFormatterPro.ankiaddon

FASE 2:

Agregar Smart Paste.

FASE 3:

Agregar editor de tablas.

FASE 4:

Agregar herramientas avanzadas.

Cada fase debe terminar con una versión instalable.

====================================================
CONTROL DE PROYECTO
===================

Crear siempre:

PROJECT_STATUS.md

Debe indicar:

Versión actual.

Funciones terminadas.

Funciones pendientes.

Errores conocidos.

Próximo paso.

====================================================
SI LLEGAS AL LÍMITE DE TOKENS
=============================

NO continúes escribiendo sin entregar.

Primero:

1. Guarda todos los archivos completos creados.

2. Actualiza PROJECT_STATUS.md.

3. Actualiza CHANGELOG.md.

4. Genera ZIP instalable.

5. Genera ANKIADDON instalable.

Después continúa desde esa versión.

====================================================
ENTREGA FINAL
=============

El resultado final debe ser:

Un complemento Anki real.

Ligero.

Rápido.

Seguro.

Compatible con Anki 25.09.

Que mejore mi flujo actual sin reemplazarlo.

El usuario siempre tiene el control.

El contenido médico nunca se modifica.
