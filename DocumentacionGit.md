## Capacitación GIT
**Este instructivo se genera con el objetivo de crear un paso a paso que nos permita utilizar GIT como sistema de control de versiones.  
Se va a realizar los pasos correspondientes para la elaboración del instructivo descrita en (DocumentacionGit).  
Este instructivo inicia con la entrega de la URL del repositorio compartido.    
A continuación se presenta el paso a paso de la ejecucion de los comandos básicos de GIT y como deben ser utilizados en el proceso de versionamiento. 
**
#### Taller.
1. **Iniciar un repositorio local.**  
Git se puede usar con CMD Símbolo del Sistema. Se crea una carpeta donde vamos a almacenar la información de la carpeta ó del repositorio que se va a trabajar.

## Creación de un repositorio Local.
* Se crea una carpeta "documentos", atravez del comando "git clon" se clona la URL del repositorio.  
<FONT COLOR="red"> 
>git clone  
 http://tfs.sistran.com:8080/tfs/colombia/OficinaArquitectura/_git/CapacitacionGit 
</FONT>  

![Con Version](./Img/Git_01.png "Clonar")
* Se valida la carpeta documentos, revisando que el contenido de la URL quede descargado, esta carpeta tambien debe contener la carpeta oculta .git.
![Con Version](./Img/Git_02.png "Versiones")  
* ### Comando para iniciar un repositorio local.   
Para iniciar un repositorio local sin necesidad de clonar un repositorio remoto se usa el siguiente comando.
<FONT COLOR="red">
> git init   
</FONT>
* ### Configurar Nombre y Correo Electrónico
<FONT COLOR="red">  

>git config --global user.name "hmunevar"  
>git config --global user.email "hmunevar@sistran.com"  
</FONT>
![Con Version](./Img/Git_03.png "Versiones")   
*Si ya tenía configurado git, puede saltarse esta sección.* 
 * ### Configure las preferencias de fin de línea.  
 Esto se debe a que Windows utiliza retorno-de-carro y salto-de-linea para marcar los finales de línea de sus archivos. Mientras que Mac y Linux utilizan solamente el caracter de salto-de-linea.  
<FONT COLOR="red"> 
>git config --global core.autocrlf true  
>git config --global core.safecrlf true  
</FONT>  
* **Listado de configuraciones: muestra historial de la configuración realizada**   
<FONT COLOR="red">  
 > git config --global --list  
</FONT> 
 ![Con Version](./Img/Git__03.png "")  

* **GIT STATUS: Indica el estado del repositorio.**  Muestra los archivos que están pendiente por subir. 
<FONT COLOR="red">  
 > git status   
</FONT> 
![Con Version](./Img/Git_05.png "muestra diferencias")   
En la carpeta va el proyecto ó documentos que se van a versionar, en este caso muestra DocumnetacionGit.md y la carpeta Img.
* **GIT ADD:Agregar archivos a nuestro proyecto,**  Es sensitivo a Mayúsculas ó minúsculas.  
<FONT COLOR="red"> 
> git add DocumentacionGit.md  
</FONT>
![Con Version](./Img/Git_06.png "adiciona archivo especifico")  

Muestra que se adiciono el documento y que esta pendiente por adicionar la carpeta img.
* **Agregar todos los archivos pendientes por proteger: Git add -A**  
<FONT COLOR="red"> 
> git add -A    
</FONT>
![Con Version](./Img/Git_07.png "adiciona todo")  
<FONT COLOR="red"> 
> git status  
</FONT>Muestra que se agrego la carpeta con todos los archivos que tenia.
* **Agregar mensaje: Git commit -m,**  Guardar los cambios con un mensaje para identificarlos.  
<FONT COLOR="red">
 > git commit -m "Se genera primera subida de 
 DocumentacioGit.md..."  
 </FONT>
* **Listar todos los commits:**  Nos da una lista de todos nuestros commits con su respectiva información.  
<FONT COLOR="red">
> git log  
 </FONT>
![Con Version](./Img/Git_08.png "Muestra los commits")  

Muestra información del Autor, correo, la fecha, hora, mensaje de cada commit y un *código que identifica cada commit (codigo Sha1).*  

**Crear Listas de log:**  Crea un archivo txt de los commits con su respectiva información.  
 <FONT COLOR="red">
> git log > Commints.txt -- Crea la lista  
> git log  
 </FONT>
![Con Version](./Img/Git_09.png "Muestra los commits")  
* **Añadir contenido: Git stage**
 Añadir contenido de archivo al área de clasificación, es un sinónimo de Git add  
 <FONT COLOR="red">
 > git stage  
  </FONT>
 ![Con Version](./Img/Git_10.png "Stage") 
 ![Con Version](./Img/Git_11.png "status")   
  ![Con Version](./Img/Git_12.png "Muestra los 
 commits")   
 * **Realizar commit:**
 Guardar los cambios con un mensaje para identificarlos.  
 <FONT COLOR="red"> 
 > git commit -m "Se realiza commit de actualización de imágenes"  
   </FONT>
  ![Con Version](./Img/Git_14.png "Muestra los 
 commits")   
* **Mostrar todos los Commit**
 Con Git Log nos muestra todos los commit con sus mensajes.  
  <FONT COLOR="red">
 > git log  
   </FONT>  
 ![Con Version](./Img/Git_15.png "Codigo Cha") 
* **Viajar a cualquier commit**
 Con Git Checkout nos permite movernos al commit que se desee.   
  <FONT COLOR="red">
 > git Checkout   
 </FONT>
 ![Con Version](./Img/Git_16.png "Movernos")
* **Viajar al último commit**
 Con Git Checkout master permite movernos al último commit.  
 <FONT COLOR="red">
 > git Checkout master  
 </FONT>
 ![Con Version](./Img/Git_17.png "Ir a master")  
 #### Ramas:.
* **Rama es una línea de tiempo en nuestro proyecto, que nos sirve para arreglar errores, experimentar, hacer grandes cambios. Que no afecte nuestro proyecto actual**  
* **La rama master es cuando realizamos -git ini, se crea esta rama por default. Es la rama principal y la rama estable del proyecto.**  
<FONT COLOR="red">
 > git branch   
 </FONT>
 **Nos muestra todos las ramas creadas.**  
   ![Con Version](./Img/Git_18.png "Versiones")  
   **Crear nuevo branch:**  Crea un archivo txt de los commits con su respectiva informaciónn.  
    <FONT COLOR="red">
> git branch Testbranch </FONT> - Nombre como va a quedar la rama.  

  Se consulta los branch creados y luego crearmos un nuevo branch.
  ![Con Version](./Img/Git_19.png "Nuevo branch Testbranch")  


**Al movernos en las distintas ramas se puede notar que cada una tiene una version distinta.** 
![Con Version](./Img/Git_23.png "Version1")  
![Con Version](./Img/Git_24.png "Version2") 
### Eliminar una Rama.   
<FONT COLOR="red">
  git branch -D TestBranch.  
   </FONT>  

  ![Con Version](./Img/Git_54.png "Eliminar rama") 

## Fusiones:
* **Es la creacion de un nuevo Commit juntando una rama con otra.**  
* **Situarnos en la rama que va a absorver.**  
<FONT COLOR="red">
 > git merge master - Desde la rama FeatureInstall se absorve lo que tenia la rama master.  
 </FONT> 
 **Nos muestra la información del merge realizado.**  
   ![Con Version](./Img/Git_25.png "Merge")  
 **Crear una Rama y quedar en ella al mismo tiempo:** Se crea la nueva rama y quedamos en ella sin necesidad de usuar el checkout.   
 <FONT COLOR="red">
 > git checkout -b TestBranch
 </FONT>   
  ![Con Version](./Img/Git_55.png "Crear")  

  **Git Remote:**  Generar la misma version de lo que esta en el Hub con lo que esta en su PC´s.  
    <FONT COLOR="red">  
> git remote add origin  http://tfs.sistran.com:8080/tfs/colombia/OficinaArquitectura/_git/CapacitacionGit   
> git remote -v </FONT>


![Con Version](./Img/Git_56.png "Crear") 

 # SourceTree:
**Sourcetree simplifica la forma en que interactúa con sus repositorios Git.**  

Repositorio compartido de Team Explorer-Connect.  

![Con Version](./Img/Git_32.png "Merge")  
#### Instalar SourceTree.  
**Despues de tener la URL del proyecto, se puede clonar, adicionar a SourceTree.** 
![Con Version](./Img/Git_34.png "Merge")
* **Clonar para descargar todo el proyecto que se encuentra con una versión estable, se usa para no contribuir, no cambiar en el proyecto.** 
* **Add es para adicionar lo que tenemos en nuestra maquina con lo que está en el proyecto.**  
 ### SourceTree interfaz grafica:
![Con Version](./Img/Git_35.png "interfaz grafica")  
![Con Version](./Img/Git_36.png "interfaz grafica")  
 ### SourceTree interfaz grafica:  
 Se puede dirigir a cualquiera de las ramas o cualquiera de los branch con doble click. 
![Con Version](./Img/Git_37.png "Branch")  
**Relacionar con nuestro repositorio remoto que está creado en VS.**  
![Con Version](./Img/Git_32.png "Repositorio")
![Con Version](./Img/Git_40.png "Repositorio")  
![Con Version](./Img/Git_41.png "Seleccionar versión")  
* **Se realiza Push para subir al repositorio.** 
* **Se Selecciona el branch que se necesita consultar el estado actual, nos indica que archivos están pendientes por protejer.**  
* **Stage All, selecciona todos los archivos que se dejan en un estado intermedio listos para subir al repositorio.**   

 ![Con Version](./Img/Git_42.png "Seleccionar versión")
![Con Version](./Img/Git_43.png "Seleccionar versión")
![Con Version](./Img/Git_44.png "Seleccionar versión")  
![Con Version](./Img/Git_45.png "Seleccionar versión")  
