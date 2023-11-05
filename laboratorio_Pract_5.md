# Creación de Ramas en Git

## Objetivo
- Aprender a crear y trabajar con ramas en Git para desarrollar características o arreglar errores en un ambiente aislado sin afectar la rama principal (`master`).

## Herramientas necesarias
- Un sistema con Git instalado.
- Acceso a un repositorio local y remoto de Git.

## Procedimiento

### 1. Verificar el Estado Actual del Repositorio
   - **Paso 1**: Ejecuta el siguiente comando para visualizar las ramas existentes y la historia de commits:
     ```bash
     git log --oneline --all --graph
     ```

### 2. Crear Ramas usando `git checkout -b ...`
   - **Paso 1**: Crea una nueva rama llamada `rama1` a partir del commit etiquetado como `v1`, y cambia a esa rama:
     ```bash
     git checkout -b rama1 v1
     ```
   - **Paso 2**: Realiza algunos cambios en esta rama y registra un nuevo commit.

### 3. Crear Ramas en Modo Despegado (Detached HEAD)
   - **Paso 1**: Cambia al commit `v1`:
     ```bash
     git checkout v1
     ```
   - **Paso 2**: Realiza algunos cambios y registra un nuevo commit.
   - **Paso 3**: Ahora, para no perder estos commits, crea una nueva rama llamada `rama2`:
     ```bash
     git checkout -b rama2
     ```

### 4. Crear Ramas usando `git branch ...`
   - **Paso 1**: Desde la rama `rama2`, crea dos nuevas ramas llamadas `licencia` y `autor` a partir de la rama `master`:
     ```bash
     git branch licencia master
     git branch autor master
     ```
   - **Paso 2**: Cambia a la rama `licencia` y crea un nuevo archivo llamado `LICENSE` con el contenido `GPL v3`, luego registra un nuevo commit:
     ```bash
     git checkout licencia
     echo "GPL v3" > LICENSE
     git add LICENSE
     git commit -m "Nuevo archivo LICENSE"
     ```
   - **Paso 3**: Cambia a la rama `autor`, crea un nuevo archivo llamado `AUTHOR` con tu nombre, modifica el archivo `README.md` y registra un nuevo commit:
     ```bash
     git checkout autor
     echo "<PON AQUÍ TU NOMBRE>" > AUTHOR
     # Suponiendo que estás usando nano para editar README.md
     nano README.md
     git add AUTHOR README.md
     git commit -m "Nuevo archivo AUTHOR y editado README.md"
     ```

### 5. Subir Ramas al Repositorio Remoto
   - **Paso 1**: Sube todas las ramas al repositorio remoto:
     ```bash
     git push origin --all
     ```

## Notas Adicionales
- Al crear ramas, estás proporcionando un ambiente seguro para experimentar sin afectar la rama principal.
- Siempre puedes visualizar el gráfico de ramas en GitHub bajo la pestaña Insights y luego en la opción Network.
- No elimines los repositorios local ni remoto, ya que se utilizarán en actividades futuras.

## Evaluación
- Subir un documento a classroom con capturas de pantalla y explicaciones sobre los procedimientos seguidos para crear y trabajar con ramas en Git.

