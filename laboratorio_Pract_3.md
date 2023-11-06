# Trabajando con el Archivo `.gitignore` en un Proyecto Node.js

## Objetivo
- Familiarizarse con el archivo `.gitignore` y aprender cómo usarlo para ignorar archivos y directorios específicos en un repositorio Git.
- Crear una aplicación simple en Node.js.

## Herramientas necesarias
- Un sistema con Git y Node.js instalados.
- Acceso a un repositorio local de Git.

## Procedimiento

### 1. Creación de una Aplicación Node.js
   - **Paso 1**: Asegúrate de estar en el repositorio que has estado utilizando en actividades anteriores.
   - **Paso 2**: Inicializa una nueva aplicación Node.js con el siguiente comando:
     ```bash
     npm init -y
     ```
   - **Paso 3**: Crea un archivo `index.js` con un simple "Hola Mundo":
     ```javascript
     console.log('Hola Mundo');
     ```
   - **Paso 4**: Ejecuta la aplicación con:
     ```bash
     npm install express
     node index.js
     ```

### 2. Añadiendo Archivos al Repositorio Local
   - **Paso 1**: Ejecuta `git diff HEAD` para intentar ver los cambios, pero notarás que no se muestra nada ya que `git diff HEAD` solo muestra cambios en archivos rastreados.
   - **Paso 2**: Utiliza `git status` para ver los archivos sin seguimiento (untracked files).

### 3. Configuración del Archivo `.gitignore`
   - **Paso 1**: Crea un archivo `.gitignore` para especificar los archivos y directorios que Git debe ignorar. Para este proyecto, ignoraremos la carpeta `node_modules` y el archivo `package-lock.json`:
     ```plaintext
     node_modules/
     package-lock.json
     ```
   - **Paso 2**: Guarda el archivo `.gitignore` y verifica que la carpeta `node_modules` y el archivo `package-lock.json` ya no aparezcan en el output de `git status`.
   - **Paso 3**: Ahora añade todos los archivos (excepto los ignorados) al área de preparación y realiza un commit:
     ```bash
     git add .
     git commit -m "Código fuente inicial"
     ```

### 4. Subir Cambios al Repositorio Remoto
   - **Paso 1**: Sube los cambios al repositorio remoto:
     ```bash
     git push
     ```
   - **Paso 2**: Crea una etiqueta para el commit actual y súbelo a GitHub:
     ```bash
     git tag v3
     git push --tags
     ```
   - **Paso 3**: Accede a tu repositorio en GitHub y verifica que se han creado las nuevas etiquetas y que el código fuente se ha subido correctamente, sin incluir la carpeta `node_modules` ni el archivo `package-lock.json`.

## Notas Adicionales
- La carpeta `.git` nunca se muestra en GitHub.
- No elimines los repositorios local ni remoto, ya que se utilizarán en actividades futuras.

## Evaluación
- Revisión del documento subido a Classroom con capturas de pantalla de los comandos ejecutados y del repositorio en GitHub.
- Discusión en clase sobre la importancia del archivo `.gitignore` y cómo ayuda a mantener el repositorio limpio y organizado.
