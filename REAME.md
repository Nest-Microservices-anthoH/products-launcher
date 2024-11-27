## Dev

1. Clonar el repositorio
2. Crear un .env basado en el .env.template
3. Ejecutar el comando `docker-compose up --build`

## Pasos para crear los Git Submodules

1. Crear un nuevo repositorio e Github
2. Clonar el repositorio en la maquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-modulo (no debe de existir en el proyecto)

```
git submodule add <repository_url> <directory_name>
```

4. Añadir los cambios al repositorio (git add, git commit , git push) Ej:

```
git add .
git commit -m "Add submodule"
git push
```

5. Inicializar y actualizar Sub-módulos, cuando alguien clone el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos

```
git submodule update --init --recursive
```
6. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```