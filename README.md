* docker build . -t marlon/orbis-training-docker:0.1.0 
* docker tag marlonric/orbis-training-docker:0.1.0 marlonric/orbis-training-docker:0.2.0

- Archivo README.md

- Archivo docker-compose.yml

``` yml
version: "2"
services:
    nginx:
      container_name: orbis-training-docker
      image: marlonric/orbis-training-docker:1.0.0
      ports:
        - "1080:80"
```

`docker-compose up -d`

mkdir makefiles | mv *.mk makefiles

    ¿Qué significa el comando -d?
Evalua si existe un directorio

    ¿Porqué la sentencia comienza con @?
Oculta el comando que lo ejecuta y solo muestra el resultado

    ¿Para qué sirve el comando mkdir?
Crea un nueva carpeta

    Explicar lo que hace la función mkdir_deploy_dir
Si no existe el folder en el GIT_BRANCH_DIR lo genera



    ¿Para qué sirve el uso de \?
Te da un salto de linea sin romper el comando
    ¿Para qué sirve el uso de &&?
concatena comandos
    ¿Qué función cumple usar los argumentos -rf?
elimina directorio recurisivamente y forzado

    Explicar lo que hace la función git_init (linea por linea)
entra al directorio nombrado en la variable GIT_BRANCH_DIR y elimina su contenido dentro $(GIT_BRANCH_DIR)/.git


         
