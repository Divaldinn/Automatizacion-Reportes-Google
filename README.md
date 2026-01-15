# Sistema de Automatización de Reportes (Google Workspace)

Herramienta empresarial desarrollada en Google Apps Script para eliminar la entrada manual de datos. Conecta automáticamente la recolección de información (Forms) con la generación de documentos oficiales (Slides/PDF) y su distribución (Gmail).

## 🚀 Flujo de Trabajo Automático

1.  **Entrada:** El usuario llena un reporte de servicio en **Google Forms**.
2.  **Procesamiento:** El script detecta el envío (`onSubmit`), captura las respuestas y procesa la fecha/hora.
3.  **Generación:** Abre una plantilla de **Google Slides**, busca variables (ej. `{{Cliente}}`) y las reemplaza con los datos reales.
4.  **Exportación:** Convierte la presentación finalizada a **PDF**.
5.  **Entrega:** Envía el PDF automáticamente por correo electrónico al cliente o supervisor.

## 🛠️ Tecnologías Usadas

* **Lenguaje:** Google Apps Script (JavaScript ES6).
* **APIs:** DriveApp, SlidesApp, MailApp, SpreadsheetApp.
* **Integración:** Google Workspace (Forms, Sheets, Slides, Gmail).

## 📄 Estructura del Código

El archivo principal contiene funciones para:
* `onFormSubmit(e)`: Trigger principal.
* `createNewPresentation()`: Copia la plantilla base.
* `replaceText()`: Lógica de búsqueda y reemplazo en diapositivas.
* `sendEmail()`: Distribución del adjunto.
