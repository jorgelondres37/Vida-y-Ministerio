# 📖 Programa Vida y Ministerio — Congregación Curauma

Herramienta web para organizar mensualmente el programa de la reunión **Vida y Ministerio Cristianos**: asigna partes de forma automática y ordenada, genera el PDF listo para imprimir, y lleva el seguimiento de quién cumplió su asignación.

> 🙏 **Sin fines de lucro.** Este proyecto se hizo únicamente para aportar a la organización y facilitar el trabajo del hermano encargado de las asignaciones. No tiene fines comerciales ni recopila datos con otro propósito.

---

## ✨ ¿Qué hace?

- 📋 **Registro de hermanos** (`index.html`): mantiene la lista de publicadores, sus restricciones y qué asignaciones puede dar cada uno.
- 🗓️ **Programa mensual** (`programa.html`): pegas el texto de la guía de *Vida y Ministerio* y la página reparte automáticamente las partes entre los hermanos habilitados, evitando que se repitan siempre los mismos.
- 🖨️ **Formato oficial e imprimible**: cada semana se genera con el mismo diseño del programa impreso, lista para exportar a PDF.
- ✅ **Seguimiento**: marca quién cumplió, quién no y quién lo reemplazó.
- 📊 **Estadísticas de confiabilidad**: porcentaje de cumplimiento, cuántas veces le ha tocado a cada hermano, y quiénes están disponibles para un reemplazo sin repetir siempre a los mismos.

---

## 🔒 Privacidad

- La página solo guarda **nombres y sus restricciones de asignación** (`data.json`) y el **historial de programas** (`programas.json`). No se guarda información sensible (edades, contactos, direcciones, etc.).
- Toda la información vive **en tu propio repositorio de GitHub**, bajo tu control. Si la congregación prefiere mayor privacidad, se recomienda usar un **repositorio privado** en vez de público.
- El token de acceso a GitHub se guarda **solo en el navegador de tu dispositivo** (nunca se sube al repositorio ni se comparte).
- Nadie más puede editar los datos sin ese token.

---

## 🚀 Cómo usarla

### 1️⃣ Conectar con GitHub (solo la primera vez)
1. Abre `index.html` (la página de **Registro**).
2. Pulsa **⚙️ Conexión GitHub** al final de la página.
3. Genera un token en GitHub: *Settings → Developer settings → Fine-grained tokens*, con permiso **Contents: Read and write**, y pégalo ahí junto con tu usuario y el nombre del repositorio.

### 2️⃣ Mantener el registro de hermanos
- En `index.html` agrega o edita a los hermanos, sus restricciones y qué asignaciones puede dar cada uno.
- Los cambios se guardan directo en `data.json` de tu repositorio.

### 3️⃣ Generar el programa del mes
1. Abre `programa.html` y toca **Programa**.
2. Copia el texto de la guía de *Vida y Ministerio* (desde el PDF) y pégalo en el cuadro.
3. Presiona **Leer y asignar** 🪄. La página reparte las partes automáticamente respetando las restricciones y el historial.
4. Revisa y edita lo que necesites: cada nombre es editable.
5. Pulsa **Guardar en historial** para que quede registrado en `programas.json`.
6. Usa **Imprimir / PDF** para exportar el programa con el formato oficial.

### 4️⃣ Seguimiento de asignaciones ✅
1. Ve a la pestaña **Seguimiento**.
2. Toca el nombre de cada asignación y marca si **cumplió**, **no cumplió** (indicando quién lo reemplazó) o quedó **confirmada**.
3. Guarda los cambios con **Guardar seguimiento**.
4. Revisa la sección de **estadísticas** para ver el porcentaje de cumplimiento de cada hermano y quiénes están disponibles para un reemplazo.

---

## 📁 Estructura del repositorio

| Archivo | Contenido |
|---|---|
| `index.html` | Registro de hermanos y sus restricciones |
| `programa.html` | Generador del programa mensual, PDF y seguimiento |
| `data.json` | Lista de hermanos (se genera/edita desde `index.html`) |
| `programas.json` | Historial de meses guardados con sus asignaciones y seguimiento |

---

## ⚠️ Nota sobre antivirus

Algunos navegadores o antivirus pueden marcar `programa.html` como sospechoso al descargarlo, por ser un archivo con código que se conecta a GitHub para guardar datos. Es una **falsa alarma**: solo se conecta a `api.github.com` y a Google Fonts, nada más.

---

Hecho con ❤️ para servir a la congregación.
