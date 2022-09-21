# EXAMEN PARTE 1


##  Repositorio RA
1. Primero se hizo la configuracion para definir el nombre de usuario.
2. Posicionarse en la carpeta **RA** para inicializar el repositorio.
3. Ejecutar el comando *git remote add URL* para agregar el repositorio remoto creado en GITHUB
```
$ git config --global user.name "JocelynRdzPon"

$ git config --global user.email "jocerdzp26@gmail.com"

$ cd RA

$ git init
Initialized empty Git repository in C:/EXAU1/RA/.git/

$ git remote add origin https://github.com/JocelynRdzPon/RA.git
```

![Imagen](./CAPTURAS/C1.png) <br>

## README

1. Se creo el archivo **README.md** con el comando 
```
$ touch README.md
```
<br>

-----------------------
![Imagen](./CAPTURAS/C2.png)



-----------
## Commit inicial

1. Se comienza a editar el archivo, agregando las capturas y fragmentos de comandos utilizados. 

![Imagen](./CAPTURAS/C4.png)<br>

2. Se realiza el ***commit inicial***
```
$ git add .

$ git commit -m "commit inicial"
```
![Imagen](./CAPTURAS/C5.png)<br>

--------------
## Push inicial

1. Se escribira el comando:
```
git push origin master
```
Se procede a ejecutarlo

![Imagen](./CAPTURAS/C6.png)<br>

2. Se verifica en el repositorio remoto para ver los cambios.
![Imagen](./CAPTURAS/C7.png)<br>

-------------------
## Ignorar archivos

1. Se creo el archivo *privado.txt*
```
$ touch privado.txt
```
2. Se creo la carpeta *privada*
```
$ mkdir privada
```
3. Se creo el archivo  ***.gitignore***
```
$ touch .gitignore
```
4. Se consulta el estado del repositorio y se pueede visualizar que se encuentra en *Untracked* el archivo *privado.txt*
```
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        privado.txt
```
![Imagen](./CAPTURAS/C8.png)<br>


5. Se procede a escribir en el archivo ***.gitignore*** las lineas para establecer que se ignoren los archivos ***privado.txt*** y la carpeta ***privada***
![Imagen](./CAPTURAS/C9.png)<br>

6. Al guardar el archivo *.gitignore* (CTRL+S), se vuelve a consultar el estado del repositorio y se visualiza que el archivo *privado.txt* ya no se encuentra en Staged

![Imagen](./CAPTURAS/C10.png)<br>

-----------------------
## Añadir archivo1.txt

Se creo el archivo1.txt y se realizo el add y commit
```
$ touch archivo1.txt

$ git add .

$ git commit -m "Se agrego archivo1.txt"
```

![Imagen](./CAPTURAS/C11.png)<br>

------------------
## Crear el tag v0.1 
1. Se crea el tag con el nombre ***v0.1***. 
```
$ git tag -a v0.1 -m "Tag v0.1"
```
2. Se comprueba que se haya creado correctamente con el comando:
```
$ git tag
```
![Imagen](./CAPTURAS/C12.png)<br>

------------------

## Subir el tag v0.1 

Para subir el tag creado al repositorio remoto se ejecutaran el comando:
```
$ git push origin --tags
```
![Imagen](./CAPTURAS/C14.png) <br>

Se ejecutara y al revisar en el repositorio remoto en el apartado de *Tags*
![Imagen](./CAPTURAS/C15.png) <br>

Se visualizara de la siguiente manera
![Imagen](./CAPTURAS/C13.png) <br>

-----------------------
## Crear una rama v0.2 

1. Se creo la rama v0.2. 
```
$ git branch v0.2
```
![Imagen](./CAPTURAS/C16.png) <br>
2. Posiciona tu working directory en esta rama.
```
git checkout v0.2
```
![Imagen](./CAPTURAS/C17.png) <br>

## Añadir Archivo 2.txt

1. Se añadio un archivo2.txt en la rama v0.2 con el comando:
```
$ touch archivo2.txt
```
 
![Imagen](./CAPTURAS/C18.png) <br>

---------------

## Crear rama remota v0.2 

