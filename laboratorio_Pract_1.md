
# Laboratorio de Práctica con Git: USO BÁSICO DE GIT

## Introducción

Git es un sistema de control de versiones distribuido que permite a los desarrolladores colaborar en proyectos de software. Con Git, puedes rastrear los cambios en el código fuente durante el desarrollo, y trabajar en diferentes ramas para mantener organizadas las características y las correcciones de errores.

## Configuración Inicial

1. Configura tu nombre y correo electrónico en Git con los siguientes comandos:
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@example.com"
```

## Ejercicios

### Ejercicio 1: Creación de un Repositorio Local

1. Crea una nueva carpeta en tu máquina local llamada `mi-proyecto`.
2. Navega a `mi-proyecto` en la terminal.
3. Inicializa un nuevo repositorio Git con el siguiente comando:
```bash
git init
```

### Ejercicio 2: Haciendo Cambios

1. Crea un nuevo archivo llamado `readme.md`.
2. Escribe algo en `readme.md`, por ejemplo: "Este es mi primer proyecto en Git".
3. Añade elementos en markdown por lo menos 5 elementos distintos: título, links, imágenes desde URL, tabla y listas
5. Agrega `readme.md` al área de stage con el siguiente comando:
```bash
git add readme.md
```
4. Comete los cambios con el siguiente comando:
```bash
git commit -m "Añadido readme.md"
```

### Ejercicio 3: Verificando el Estado y el Historial

1. Verifica el estado de tu repositorio con el siguiente comando:
```bash
git status
```
2. Muestra el historial de commits con el siguiente comando:
```bash
git log
```
3. Copialo y pégalo en el fichero readme.md haz un add y un commit con el cambio

### Ejercicio 4: Navegación entre Commits

1. Usa `git log` para encontrar el hash de un commit anterior.
2. Navega a ese commit con el siguiente comando:
```bash
git checkout <hash-del-commit>
```
Añade el comando y la salida del comando de git checkout al readme.md, commitealo.

RECUERDA: estar siempre en master cuando realices commits porque sino el commit que hagas estará descolgado del árbol principal

3. Navega de regreso a la rama `master` con el siguiente comando:
```bash
git checkout master
```

### Ejercicio 5: Etiquetando y Borrando Etiquetas

En Git, las etiquetas se utilizan para marcar puntos específicos en el historial del repositorio, como una versión particular de un software. A continuación, se muestra cómo crear y eliminar etiquetas en Git.
Las etiquetas son útiles para ponerle una especie de nombre a un commit, bien porque es necesario recordarlo o bien porque ese cambio es importante.

1. Crea una etiqueta para el commit actual con el siguiente comando:
```bash
git tag v1.0
```
2. Borra la etiqueta con el siguiente comando:
```bash
git tag -d v1.0
```
3. Crea dos etiquetas en dos commits diferentes

### Ejercicio 6: Visualizando Diferencias
El comando git diff permite ver las diferencias entre los archivos en tu área de trabajo, el área de preparación, y los commits. Las líneas eliminadas se mostrarán con un signo menos (-), y las líneas añadidas se mostrarán con un signo más (+).

1. Realiza un cambio en `readme.md`.
2. Usa el siguiente comando para ver las diferencias entre el archivo modificado y la última versión comiteada:
```bash
git diff
```
3. Copia la información que obtienes en el fichero readme.md con el título del ejercicio y commitea.
4. Busca las diferencias de las dos etiquetas creadas en diferntes commits en el ejercicio anterior en el último punto.
5. 3. Copia la información que obtienes en el fichero readme.md con el título del ejercicio y commitea.
  
### Ejercicio 7: Subiendo tu Proyecto a GitHub

1. Una vez que hayas iniciado sesión, haz clic en el botón New en la esquina superior izquierda para crear un nuevo repositorio.
2. Dale un nombre a tu repositorio, por ejemplo, mi-proyecto.
3. Deja las demás opciones como están y haz clic en el botón Create repository.
Sigue los comandos serán algo como lo siguiente:

```bash
git remote add origin https://github.com/tu-usuario/mi-proyecto.git
git branch -M main
git push -u origin main
```


## Conclusión

¡Bien hecho! Has completado el laboratorio básico de Git. Ahora tienes una comprensión básica de cómo crear un repositorio, hacer cambios, ver el historial, navegar entre commits, etiquetar commits y ver diferencias entre

## ENTREGA: EL LINK DEL REPOSITORIO.
