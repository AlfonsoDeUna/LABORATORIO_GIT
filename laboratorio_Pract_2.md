# Deshacer Cambios en un Repositorio Local con Git

## Objetivo
Aprender cómo deshacer cambios en diferentes etapas del flujo de trabajo de Git.

## Herramientas necesarias
- Un sistema con Git instalado.
- Acceso a un repositorio local de Git.

## Procedimiento

### 1. Deshacer Cambios en el Directorio de Trabajo
   - **Paso 1**: Asegúrate de estar en el último commit de la rama `master`.
   - **Paso 2**: Modifica el archivo `README.md` eliminando las 2 últimas líneas utilizando el comando:
     ```bash
     nano README.md
     ```
   - **Paso 3**: Verifica los cambios realizados con el comando:
     ```bash
     git diff HEAD
     ```
     Este comando muestra las diferencias entre el directorio de trabajo y el último commit.
   - **Paso 4**: Para revertir los cambios, ejecuta:
     ```bash
     git reset --hard
     ```
     Este comando restaura los archivos en el directorio de trabajo al estado del último commit.

### 2. Deshacer Cambios en el Área de Preparación (Staging Area)
   - **Paso 1**: Tras modificar el archivo `README.md` y agregarlo al área de preparación con:
     ```bash
     git add README.md
     ```
   - **Paso 2**: Si deseas deshacer estos cambios, ejecuta nuevamente:
     ```bash
     git reset --hard
     ```

### 3. Deshacer un Commit
   - **Paso 1**: Crea cambios en el fichero y añádelos al área de preparación y luego has realizado un commit con:
     ```bash
     git commit -m "Borrar líneas de README.md"
     ```
   - **Paso 2**: Para deshacer este commit, ejecuta:
     ```bash
     git reset --hard HEAD~1
     ```
     - `HEAD~1` indica el commit anterior al actual. 
     - `HEAD~2` serían 2 commits atrás, y así sucesivamente.

## Notas Adicionales
- Utilizar `git reset --hard` con cuidado, ya que elimina los cambios del directorio de trabajo y del área de preparación, y puede eliminar commits si se usa con los modificadores `HEAD~n`.
- Evitar borrar los repositorios locales o remotos, ya que serán utilizados en actividades futuras.
- Subir un documento a classroom con las capturas de pantalla de los comandos ejecutados y explicaciones de lo aprendido.

