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