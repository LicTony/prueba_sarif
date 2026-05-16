# prueba_sarif
Prueba de un archivo .sarif

## ¿Qué es un archivo .sarif?

SARIF (Static Analysis Results Interchange Format) es un formato estándar (basado en JSON) utilizado para reportar y compartir los resultados de herramientas de análisis estático (como Checkmarx, SonarQube, etc.). Permite que diferentes herramientas de seguridad interactúen con otros sistemas, como GitHub o editores de código, de manera unificada.

## ¿Cómo utilizar este archivo?

A continuación te explico cómo puedes ver y utilizar los resultados de un archivo `.sarif` con ejemplos prácticos.

### 1. En GitHub (Recomendado)

Esto es lo que más se parece a lo que verás cuando uses Checkmarx One de verdad integrado en un flujo de trabajo.

1. Crea un repositorio en GitHub (puede ser público o privado).
2. En la raíz del repositorio crea una carpeta llamada `.github`.
3. Dentro de `.github` crea otra carpeta llamada `sarif`.
4. Guarda tu archivo (por ejemplo, `checkmarx-example.sarif`) dentro de esa carpeta.
5. Sube los archivos a GitHub (`commit` + `push`).
6. Ve a tu repositorio en GitHub → pestaña **Security** → **Code scanning** (en el menú izquierdo).

GitHub detectará automáticamente el archivo y te mostrará las alertas como si las hubiera encontrado Checkmarx.

### 2. Abrirlo fácilmente en VS Code

1. Instala la extensión **"SARIF Viewer"** en VS Code (es la oficial de Microsoft).
2. Abre tu archivo `.sarif` con VS Code.
3. Verás un panel con la lista de problemas, colores de severidad, líneas de código marcadas, etc.

### 3. Verlo online (sin instalar nada)

Puedes subir el archivo a estos visores web gratuitos:

* [SARIF Web Viewer](https://sarifweb.azurewebsites.net/)
* [SARIF Viewer](https://www.sarifviewer.com/)

---

### Resumen: ¿Qué te recomiendo hacer ahora?

1. Crea un repositorio de prueba en GitHub.
2. Sube tu archivo `.sarif` dentro de la carpeta `.github/sarif/`.
3. Mira la sección **Security** → **Code scanning**.
