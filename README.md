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

Subir los cambios al repositorio remoto.

Mediante el comando:
```
$ git push origin v0.2
```
![Imagen](./CAPTURAS/C19.png) <br>

Se suben los cambios y se crea la rama remota en Github

![Imagen](./CAPTURAS/C20.png) <br>

-------------------
## Merge directo 

1. Posicionarse en la rama master. 
```
$ git checkout master
```
2. Hacer un merge de la rama v0.2 en la rama master. 
```
$ git merge v0.2
```
![Imagen](./CAPTURAS/C21.png) <br>

----------------

## Merge con conflicto 
1. Posicionarnos en la rama *MASTER*
```
$ git checkout master
```

2. En el ***archivo1.txt*** se escribio **Hola** y se realizo el commit
```
$ vi archivo1.txt

$ cat archivo1.txt
Hola

$ git add .

$ git commit -m "Archivo 1 MASTER"
```
![Imagen](./CAPTURAS/C22.png) <br>
![Imagen](./CAPTURAS/C23.png) <br>

3. Se procede a posicionarse en la rama v0.2
```
$ git checkout v0.2
```
4. En el ***archivo1.txt*** en la rama *v0.2* se escribio **Adios** y se realizo el commit
```
$ vi archivo1.txt

$ cat archivo1.txt
Adios

$ git add .

$ git commit -m "Archivo 1 V0.2"
```
![Imagen](./CAPTURAS/C24.png) <br>

5. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2 
 ```
 $ git checkout master

 $ git merge v0.2
 ```

 ![Imagen](./CAPTURAS/C25.png) <br>
 
 ------------------
## Listado de ramas 

1. Listar las ramas con merge y las ramas sin merge. 
 ![Imagen](./CAPTURAS/C26.png) <br>

----------------------
 ## Arreglar conflicto 

1. Se va arreglar el conflicto de **MERGING**, como se muestra en la imagen al realizar el merge se notifica que hay un *conflicto* en el *archivo1.txt* el cual se debe de resolver
   
![Imagen](./CAPTURAS/C27.png) <br>

2. Para resolverlo se hizo un add y commit al archivo, una vez hechos los cambios.
>![Imagen](./CAPTURAS/C28.png) <br>

## Borrar rama 

1. Se creo un tag para almacenar lo creado en la rama *v0.2*. Se muestran los tags existentes en el repositorio.
```
$ git tag -a v0.2 -m "Tag v0.2"

$ git tag
v0.1
v0.2
```
   >![Imagen](./CAPTURAS/C29.png) <br>

1. Se elimino la rama v0.2 con el comando 
```
git branch -d v0.2
Deleted branch v0.2 (was 1d97efd).
```
 >![Imagen](./CAPTURAS/C30.png) <br>

## Listado de cambios 

Se muestra los commits con sus ramas y cambios efectuados

 >![Imagen](./CAPTURAS/C31.png) <br>

 # EXAMEN SEGUNDA PARTE

## Cuenta de GitHub 


1. Poner una foto en tu perfil de GitHub. 
2. Poner el doble factor de autentificación en tu cuenta de GitHub. 
   ![Imagen](./CAPTURAS/C32.png) <br>
3. Añadir (si no lo has hecho aun) la clave pública (ssh) que se corresponde a tu equipo. 


## Uso social de GitHub 

1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y síguelos. 
2. Seguir los repositorios RA del resto de tus compañeros. 
3. Añadir una estrella a los repositorios RA del resto de tus compañeros. 
 ![Imagen](./CAPTURAS/33.png) <br>

## Crear una tabla 

Crear una tabla de este estilo en el fichero README.md con la información de 3 de tus compañeros de clase: 

|Nombre | GITHUB|
|-------|-------|
|AngelSebastainGarciaSosa| Ange,LSebastianGarciaSosa|
|Aisslin |diaz696|
|Geronimo Martinez|GeroimoMtz|



 

## Colaboradores 

Ponerme como colaborador del repositorio RA *mi usuario: jmav94 

 ![Imagen](./CAPTURAS/C34.png) <br>

![Imagen](./CAPTURAS/C35.png) <br>