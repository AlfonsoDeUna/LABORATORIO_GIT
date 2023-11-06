# Resolviendo Conflictos en Git

## Objetivo
- Entender qué es un conflicto en Git, cómo se produce y cómo resolverlo.

## Herramientas necesarias
- Un sistema con Git instalado.
- Acceso a un repositorio local y remoto de Git.

## Procedimiento

### 0. crea un fichero `README2.md` con una línea de título con tu nombre y la fecha de ayer
   **paso1** git add, git commit, git push . Es decir crea el fichero con un nombre y la fecha y lo subes a repositorio local y a remoto

### 1. Modificación del archivo `README2.md` en el Repositorio Remoto
   - **Paso 1**: Accede a tu repositorio en GitHub.
   - **Paso 2**: Haz clic en el archivo `README2.md` y luego en el icono del lápiz para editar el archivo.
   - **Paso 3**: Inserta una línea con un título utilizando `#` y luego añade modifica la línea de la fecha.
   - **Paso 4**: Haz clic en "Commit changes" para registrar el cambio. Puedes añadir un mensaje al commit si lo deseas.

### 2. Modificación del archivo `README2.md` en el Repositorio Local
   - **Paso 1**: Abre el archivo `README2.md` en tu repositorio local con un editor de texto, por ejemplo:
     ```bash
     nano README2.md
     ```
   - **Paso 2**: Añade una línea al final del archivo y modifica la línea de la fecha.
   - **Paso 3**: Guarda los cambios, añade el archivo al área de preparación y registra el commit:
     ```bash
     git add README2.md
     git commit -m "Actualización de README2.md"
     ```

### 3. Intento de Subir el Commit Local al Repositorio Remoto
   - **Paso 1**: Intenta subir el commit local al repositorio remoto con:
     ```bash
     git push
     ```
   - **Paso 2**: Observa que Git te indica que debes actualizar tu repositorio local antes de subir nuevos cambios.

### 4. Resolución de Conflictos
   - **Paso 1**: Ejecuta el siguiente comando para obtener los cambios del repositorio remoto:
     ```bash
     git pull
     ```
   - **Paso 2**: Al existir un conflicto en el archivo `README2.md`, Git te indicará que debes resolverlo manualmente.

### 5. Corrección del Conflicto
   - **Paso 1**: Abre el archivo `README2.md` y localiza las marcas de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`). Entre estas marcas, encontrarás las líneas conflictivas del commit local y remoto.
   - **Paso 2**: Elige una de las versiones o modifica las líneas según sea necesario para resolver el conflicto.
   - **Paso 3**: Elimina las marcas de conflicto, guarda los cambios, añade el archivo al área de preparación y registra un nuevo commit:
     ```bash
     git add README2.md
     git commit -m "Arreglado conflicto en README.md"
     ```
   - **Paso 4**: Ahora sube tu commit al repositorio remoto:
     ```bash
     git push
     ```

## Notas Adicionales
- Es recomendable hacer un `git pull` al inicio del día y un `git push` al final del día para evitar conflictos.
- No elimines los repositorios local ni remoto, ya que se utilizarán en actividades futuras.

## Evaluación
- Subir un documento a Classroom con capturas de pantalla y explicaciones de los pasos seguidos para resolver el conflicto.

