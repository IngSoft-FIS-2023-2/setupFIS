# Guía setup del ambiente VS Code :computer:
Guía para realizar el setup inicial de los ejercicios de Fundamentos de Ingeniería de Software.
**Partiendo de que se tiene una cuenta de GitHub (sino podés crearla [acá](https://github.com/signup)) vamos a ver los siguientes temas:**

 - Autenticación  
 - Cómo clonar un repositorio.

:heavy_exclamation_mark:**Esta guía no es definitiva, puede haber (es muy probable que lo haya) más de una forma de realizar algún paso teniendo el mismo efecto. Utilizá la manera en la que te sientas más comodo**

## Autenticación en VS Code :key:
Para poder usar git en conjunto con GitHub, es decir, *llevar los cambios que haga localmente a la nube (entre otras cosas)*, es necesario hacer **autenticarse**.

Esto es necesario para hacerle saber a GitHub que yo soy la persona quién dice ser y así poder tener ciertos permisos, por ejemplo: editar o clonar determinados repositorios.

Yo puedo estar logueado en GitHub, crear mi repositorio y saber que yo soy el dueño y tengo permisos, pero si mi lugar de trabajo (mi computadora) que usa Git no lo sabe, entonces no puedo hacer nada. Para esto se hace la autenticación. 

**Existen varias maneras de realizar esta autenticación, acá vamos a ver la manera de hacerlo directamente desde Visual Studio Code.**

:heavy_exclamation_mark:**Nota:**  Una vez que se hace la autenticación en una computadora, no es necesario volver a hacerlo. Pero si por algún motivo se "desloguea", solo basta seguir esta guía.

### -Paso :one:
Para poder hacer la autenticación mediante Visual Studio Code hay varios caminos. Pero para esta guía recomiendo que se creen una carpeta en algún lugar de fácil acceso y la abran con VS Code.   
<p align="center">
<img src = "https://github.com/kidnixt/setupFIS/assets/57159622/d1c35b6a-fedf-4c9b-9567-6cdfb9ac4b3b">
</p>

### -Paso :two:
Luego necesitamos abrir la terminal en nuestra IDE (VS Code). Para hacer eso vamos al menú superior donde dice "***Terminal***", luego hacemos click donde dice "***New Terminal***". Nos debería aparecer lo siguiente  
<p align="center">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/88bc86c8-4834-447d-b633-a533331e23ac">
</p>

**Podemos ver que tenemos una terminal que ya está apuntando al directorio que queremos**

### -Paso :three:
En el alcance de la materia, GitHub nos puede pedir autenticarnos en dos escenarios:

 1. Clonar un repositorio privado.
 2. Aplicar cambios a un repositorio.

Vamos a partir del caso de clonar un repositorio privado, ya que es la situación del obligatorio. 
Entonces, hasta ahora tenemos nuestra carpeta abierta en VS Code, con una terminal que también está "abierta" en ese directorio (es decir, está apuntando a esa carpeta).

Procedemos a clonar un repositorio con el comando que vimos antes. Y nos saldrá lo siguiente (por lo menos en **Linux**).
<p align="center">
<img src ="https://github.com/kidnixt/setupFIS/assets/57159622/50392520-f66c-4fbe-b5bd-d949a7541786">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/5c193acd-dd65-4dd8-9cc8-ffcc7f958dbb">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/d7b82c5a-d099-4289-bd35-71cd87e2993b">
</p>

Siguiendo todos los pasos al final, en la parte inferior al hacer click en el icono de "usuario" podemos ver que efectivamente tenemos nuestro Visual Studio Code vinculado con nuestra cuenta de GitHub, y que efectivamente se clonó el repositorio. 

<p align="center">
  <img src="https://github.com/kidnixt/setupFIS/assets/57159622/d75a934a-245f-4fee-b627-fe37ab3d2cc4">
</p>

## Aclaración de autenticación en VS Code :warning:

**Solo hicimos la autenticación** usando VS Code, es decir si querés clonar o usar comandos git que tengan que ver con GitHub **fuera de VS Code**, o sea, fuera de la IDE. Por ejemplo: en una terminal externa, **NO** vas a poder. 

Te va a pedir realizar una autenticación extra con un usuario y una contraseña.
<p align="center">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/a863bd23-30c4-42a9-a4bc-d7901521bc25">
</p>

En la parte de ***username*** ponés nombre de usuario de GitHub. Y en la parte de ***password*** vas a poner tu **Personal Access Token** (se consigue en este [link](https://github.com/settings/tokens/new))

En el apartado **Note** ponés un nombre que quieras (para identificar ese token). Y en el **Expiration** seleccionas la duración del token (recomiendo poner la opción de que no expire).
<p align="center">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/18474afe-3e47-44cc-8920-1b475393ce36">
</p>

En la parte de los **Scopes** se definen los permisos que tendra ese token, recomiendo seleccionar todos (haciendo click en la casilla que está un poco hacia la izquierda se marcan todas las de ese grupo). Para finalizar haces click en el **botón verde** de abajo para crear el token. 

<p align="center">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/d711df30-918a-47b9-95ef-9cf894661750">
</p>

:heavy_exclamation_mark:**Nota:** Una vez que creamos el token debemos copiarlo y guardarlo en algún lugar ya que no podremos volver a verlo de nuevo. Si lo perdés y por algún motivo te "deslogueamos" de Github en tu computadora, tenés que crear un token nuevo.
 
## Clonar un repositorio :recycle:
En este apartado veremos la **clonación** de un repositorio, o sea, partiremos de un repositorio que ya se encuentre en GitHub (es decir, en la "nube"). Particularmente veremos la clonación mediante el protocolo **HTTPS**.

### -Paso :one:

Primero debemos tener abierto en nuestro navegador el repositorio que queremos clonar y deberiamos ver algo como esto
<p align="center">
 <img src ="https://github.com/kidnixt/setupFIS/assets/57159622/4205b6ab-762b-46a8-9ecd-bb7e7d0b9fc4">
</p>

### -Paso :two:
Luego hacemos click en el botón verde que dice **"Code"**, se nos abrirá lo siguiente:  
<p align="center">
<img src= "https://github.com/kidnixt/setupFIS/assets/57159622/5116a793-6fe7-474f-807e-2395048853dd">
</p>

### -Paso :three:
Elegimos el apartado de **HTTPS** y copiamos la dirección que nos aparece ahí. En este caso es 
```
https://github.com/torvalds/linux.git
```
### -Paso :four:
Suponiendo que ya estás autenticado en la computadora y/o terminal en la que estés trabajando y, también estás en el directorio en el que querés clonar y obtener todos los archivos del repositorio, simplemente utilizas el comando:
```
git clone <URL del Repositorio>
```

:heavy_exclamation_mark:**Nota:**  El comando no lleva los símbolos de menor y mayor.
En este caso, quedaria de la siguiente manera:
```
git clone https://github.com/torvalds/linux.git
```

### -Paso :five:
Todo lo que esté dentro del repositorio quedará dentro de una nueva carpeta que lleva el nombre del repositorio. Es decir, si yo estoy parado en el **Escritorio** y ejecuto el *git clone*. Todos los archivos quedarán en la carpeta **linux** que está en el **Escritorio**
