# Pasos para la Realización de un Pull Request

## 1. Hacer un Fork del Repositorio
- El usuario debe hacer un fork del repositorio al que desea contribuir. Esto crea una copia completa del repositorio en la cuenta de GitHub del usuario.
- Acceder al repositorio deseado y pulsar sobre el botón Fork.

## 2. Clonar el Repositorio
- Clonar el repositorio copiado a la cuenta del usuario.
- Ejecutar el comando:


## 3. Crear una Nueva Rama y Realizar Cambios
- Crear una nueva rama para realizar cambios propuestos:
```bash
git checkout -b nombre_rama
```

- Modificar el contenido necesario y hacer commit de los cambios:
```bash
git commit -am "Descripción de los cambios realizados
```


## 4. Subir Cambios al Repositorio
- Verificar el nombre del repositorio remoto, usualmente es 'origin':
```bash
git remote
```

- Subir los cambios a la rama creada en el repositorio remoto:
```bash
git push origin nombre_rama
```


## 5. Crear el Pull Request en GitHub
- En la página de GitHub, verificar la aparición de un cuadro indicando cambios en una nueva rama y crear un nuevo Pull Request.
- Pulsar el botón 'Compare & pull request'.
- Rellenar el formulario con un comentario explicativo del Pull Request y pulsar el botón 'Create pull request'.


