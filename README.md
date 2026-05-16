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
5. Crea un archivo de workflow en `.github/workflows/upload-sarif.yml` para procesar el reporte (ya lo tenés configurado en este repo).
6. Sube los archivos a GitHub (`commit` + `push`).
7. Espera a que termine la ejecución del workflow en la pestaña **Actions**.
8. Ve a tu repositorio en GitHub → pestaña **Security** → **Code scanning** (en el menú izquierdo).

GitHub leerá el archivo gracias al Action y te mostrará las alertas como si las hubiera encontrado Checkmarx de verdad. 
*(Aclaración: Si tu repositorio es privado, GitHub requiere la licencia de GitHub Advanced Security para habilitar esta pestaña).*

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

1. Crea un repositorio de prueba en GitHub (si es privado recordá lo de la licencia).
2. Sube tu archivo `.sarif` en la carpeta `.github/sarif/` junto con el workflow `.github/workflows/upload-sarif.yml`.
3. Espera a que termine el Action y mirá la sección **Security** → **Code scanning**.
