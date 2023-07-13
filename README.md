# Producction_code_Angular

Este repositorio esta reservado solamente para el proceso de produccion es decir una vez que se haya concluido la creacion de la pagina lo que se hace es
un build en nuestra aplicacion y crear una carpeta de modo automatico que por defecto se va a llamar dist (de distribution), que es la carpeta que va a tener los
archivos del despleguie:

## Comando para poner en produccion
      ng build --configuration production --aot 

El comando de arriba crea los archivos de despliegue (una carpeta en nuestro proyecto que se llamara dist.
si no queremos despleguelar en la raiz del hosting porque quizas hay otra app web en la raiz en este caso lo que se tiene que hacer es 

      ng build --configuration production --aot --base-href /nombredeCArpeta

## Usando el firebase
si estamos usando el firebase para almacenar datos de nuestra app, tenemos que ir a firebase una vez en firebase buscar en el menu: 'hosting'
una vez en hosting haga click en button 'comenzar' lo primero es instalar si queremos alojar nuestro sitio en el host de firebase.
podemos seguir las instrucciones que el site nos proporciona para executarlo. el comando es:

### Paso 1
        npm install -g -firebase-tools

 el comando de arriba lo ejecutamos en la consola del visual studio code donde si encuentra nuetsra app
 en el mismo site procedemos en dar seguiente para que nos trae las proximas instrucciones.

### Paso 2

        firebase login    --> comando para acceder a google

En seguida iniciar el proyecto con el comando (ejecuta en el directorio raiz de tu app):

          firebase init 
          
el comando de arriba nos traera varias caracteristicas y tenemos que elegir una. LA caracteristica que tenemos que elegir tiene que ser 
de acuerdo al tipo de database que estamos usando en firebase, en nuestro caso es `realtime database : c .. . . . . ` que es la que tenemos que elegir 
una vez que hayamos elegido la caracteristica presionamos la tecla ´espacio´ y nos saldra un asterisco 

La proxima caracteristica es de `Hosting: especificamente que nos dice de configurar los archivos de hosting de firebase` otra vez la tecla ´espacio´
una vez hecho eso presionamos la tecla enter.

Saldra una caja de opciones debemos selccionar la opcion:  `use an existent proyect` presiona enter y nos aparecera todos los proyectos creados.
elija la dicha base de datos.

la proxima pregunta que vendria seria que quiero utilizar como directorio publico? le pondras  `dist`

el proximo paso nos preguntara si queremos crear como una `single page` la respuesta es yes.

con estos pasos ya estaria hecho la configuracion inicial.

### Paso 3

Una vez hecho eso volvimos al firebase en el punto donde habiamos dejado, hacemos seguiente. y usamos el comando:

        firebase deploy

Una vez hecho eso ya nos tiene que ofrecer la urls para acceder desde cualquier ordenador del mundo conectado a internet a nuestro hosting

   

    
