# Fusión y Eliminación de Ramas en Git

## Objetivo
- Aprender a fusionar y eliminar ramas en Git después de haber completado el trabajo en ellas.

## Herramientas necesarias
- Un sistema con Git instalado.
- Acceso a un repositorio local y remoto de Git.

## Procedimiento

### 1. Eliminación de una Rama Local
   - **Paso 1**: Para eliminar una rama local, como `rama2`, utiliza el siguiente comando:
     ```bash
     git branch -d rama2
     ```
   - **Paso 2**: Si la rama no ha sido fusionada y deseas eliminarla de todas formas, utiliza el siguiente comando:
     ```bash
     git branch -D rama2
     ```

### 2. Fusionando Ramas Locales
   - **Paso 1**: Cambia a la rama `master`:
     ```bash
     git checkout master
     ```
   - **Paso 2**: Fusiona la rama `licencia`:
     ```bash
     git merge licencia
     ```
   - **Paso 3**: Fusiona la rama `autor`:
     ```bash
     git merge autor
     ```
   - **Paso 4**: Fusiona la rama `rama1`:
     ```bash
     git merge rama1
     ```

### 3. Subiendo Cambios al Repositorio Remoto
   - **Paso 1**: Sube todos los cambios al repositorio remoto:
     ```bash
     git push origin --all
     ```

### 4. Eliminando Apuntadores a Ramas Locales
   - **Paso 1**: Elimina el apuntador local a `rama1`:
     ```bash
     git branch -d rama1
     ```

### 5. Eliminando Apuntadores a Ramas Remotas
   - **Paso 1**: Elimina los apuntadores remotos a `rama1` y `rama2`:
     ```bash
     git push origin --delete rama1
     git push origin --delete rama2
     ```

### 6. Comprobando Cambios en el Repositorio Remoto
   - **Paso 1**: Verifica los cambios en el repositorio remoto mediante la interfaz de GitHub en la sección Insights, Network.

### 7. Tarea Propuesta
   - **Paso 1**: Vuelve a la rama `licencia`, añade contenido al archivo `LICENSE`, y registra un nuevo commit.
   - **Paso 2**: Vuelve a la rama `autor`, añade contenido al archivo `AUTHOR`, y registra un nuevo commit.
   - **Paso 3**: Integra los cambios de ambas ramas en la rama `master`.

## Notas Adicionales
- La fusión de ramas puede ser una operación simple de avance rápido (fast-forward) o una fusión de 3 vías que podría resultar en conflictos si las mismas líneas en los mismos archivos han sido modificadas en ambas ramas.
- La eliminación de una rama local o remota es una operación que debe ser realizada con cuidado para evitar la pérdida de trabajo.

## Evaluación
- Sube un documento a classroom con capturas de pantalla y explicaciones sobre los procedimientos seguidos para fusionar y eliminar ramas en Git.
```

Esta guía en formato Markdown proporciona una estructura clara y paso a paso para entender cómo realizar la fusión y eliminación de ramas en Git, junto con comandos específicos para llevar a cabo cada paso. También incluye una tarea propuesta para la práctica adicional y secciones para evaluación y notas adicionales que proporcionan un contexto y comprensión completa de la actividad.
