
# Laboratorio de Práctica con Git

## Introducción

Git es un sistema de control de versiones distribuido que permite a los desarrolladores colaborar en proyectos de software. Con Git, puedes rastrear los cambios en el código fuente durante el desarrollo, y trabajar en diferentes ramas para mantener organizadas las características y las correcciones de errores.

## Configuración Inicial

1. Instala Git en tu máquina local desde [https://git-scm.com/downloads](https://git-scm.com/downloads).
2. Configura tu nombre y correo electrónico en Git con los siguientes comandos:
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
3. Agrega `readme.md` al área de preparación con el siguiente comando:
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

### Ejercicio 4: Navegación entre Commits

1. Usa `git log` para encontrar el hash de un commit anterior.
2. Navega a ese commit con el siguiente comando:
```bash
git checkout <hash-del-commit>
```
3. Navega de regreso a la rama `master` con el siguiente comando:
```bash
git checkout master
```

### Ejercicio 5: Etiquetando y Borrando Etiquetas

1. Crea una etiqueta para el commit actual con el siguiente comando:
```bash
git tag v1.0
```
2. Borra la etiqueta con el siguiente comando:
```bash
git tag -d v1.0
```

### Ejercicio 6: Visualizando Diferencias

1. Realiza un cambio en `readme.md`.
2. Usa el siguiente comando para ver las diferencias entre el archivo modificado y la última versión comiteada:
```bash
git diff
```

## Conclusión

¡Bien hecho! Has completado el laboratorio básico de Git. Ahora tienes una comprensión básica de cómo crear un repositorio, hacer cambios, ver el historial, navegar entre commits, etiquetar commits y ver diferencias entre archivos.

---

Este esquema de laboratorio cubre los comandos básicos que mencionaste y proporciona ejercicios prácticos para que tus alumnos puedan aprender a usar Git de manera efectiva. Puedes expandir o modificar este laboratorio según sea necesario para satisfacer las necesidades de tu curso.
