# 📋 Registro de Hermanos

Panel web para consultar y editar el registro de hermanos y sus asignaciones del programa. Funciona como sitio estático en GitHub Pages: los datos viven en `data.json` y cada guardado crea un commit en este repositorio, así los cambios quedan disponibles desde cualquier dispositivo.

## 📁 Estructura

| Archivo | Función |
|---|---|
| 🌐 `index.html` | Página completa (HTML, CSS y JavaScript en un solo archivo) |
| 💽 `data.json` | Base de datos: un registro por hermano |
| 📝 `README.md` | Este documento |

## 👀 Funciones de consulta

Disponibles para cualquiera que abra el enlace, sin necesidad de token.

- 📊 **Resumen**: total de hermanos, activos, inactivos y en salud.
- 👥 **Por grupo**: barras de los grupos 1 al 5, con activos e inactivos diferenciados por color.
- 🏷️ **Por tarea**: una tarjeta por cada tarea (PTJ, PNB, AN, SM, PR, etc.) con el total y la división entre mujeres y varones.
- ✅ **Disponibilidad por asignación**: cuántos hermanos activos pueden tomar cada una de las 13 asignaciones. Si hay inactivos con esa asignación, se indican aparte.
- 🙋 **¿Quién puede tomar una asignación?**: elige una asignación y aparece la lista de hermanos activos disponibles, con su grupo y género.
- 🔍 **Listado**: tabla completa con buscador por nombre y filtros por grupo, tarea, género, estado (activo/inactivo) y asignación. Muestra cuántos resultados coinciden.
- 🌗 **Tema automático**: se adapta al modo claro u oscuro del dispositivo.

## ✏️ Funciones de edición

Aparecen solo en los dispositivos donde se configuró el token (ver más abajo).

| Botón | Qué hace |
|---|---|
| ➕ **Agregar hermano** | Abre el formulario para crear un registro nuevo. El número se asigna automáticamente. |
| 🔧 **Modo edición: ON/OFF** | Muestra u oculta la columna **Acciones** en la tabla. |
| ✏️ **Editar** (por fila) | Abre el formulario del hermano para modificar sus datos. |
| 💾 **Guardar cambios** | Sube todos los cambios pendientes a GitHub en un solo commit. |

**Campos del formulario:** nombre (formato `Apellido, Nombre`), tarea, grupo (1 a 5 o sin grupo), género (M/V), estado (activo/inactivo), marca "en salud" y las asignaciones disponibles.

🗑️ **Eliminar:** dentro del formulario de un hermano existente, con confirmación previa. Los números de los demás registros no se renumeran.

🔄 **Flujo de guardado:**
1. Editas o agregas hermanos. Cada **Guardar en la lista** aplica el cambio solo en tu pantalla y muestra "Cambios sin guardar".
2. Pulsas **Guardar cambios** para enviarlos a GitHub. Aparece "Guardado ✓" al terminar.
3. Si intentas cerrar la página con cambios pendientes, el navegador te avisa.

## 🔑 Conexión con GitHub

1. Crea un token en `https://github.com/settings/personal-access-tokens/new`:
   - **Repository access**: solo este repositorio.
   - **Permissions → Contents**: *Read and write*.
2. Abre la página, pulsa **Conexión GitHub** (al pie) y pega el token.
3. Usuario, repositorio y rama se detectan desde la URL. Si no, complétalos a mano.

Detalles:
- 🔐 El token se guarda únicamente en el `localStorage` de ese dispositivo. No se sube al repositorio.
- ⚡ Con token, la
