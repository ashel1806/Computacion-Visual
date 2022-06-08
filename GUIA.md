Si estás leyendo este artículo, ya debes conocer que abundan los beneficios de ser un contribuidor de proyectos de código abierto (Puedes saltarte este artículo y navegar hasta el final si estás aquí por la hoja de trucos).

El problema común al que se enfrenta un aspirante a contribuidor de proyecto de código abierto es como realizar el primer paso desde el  `fork`  hasta el  `pull request`. Luego de leer este artículo, estarás equipado con todo lo que necesitas para realizar el primer  `pull request`  a un proyecto de código abierto.

Aparte de hacerse fácil este proceso para ti, el flujo de trabajo definido en git también hará que tu contribución se vea profesional. Esto será en el caso que quieras agregar tu contribución a tu portafolio.

# Pre-requisitos

![2](https://www.freecodecamp.org/espanol/news/content/images/2021/05/2.png)

Photo by  [Randy Fath](https://unsplash.com/@randyfath?utm_source=ghost&utm_medium=referral&utm_campaign=api-credit)  /  [Unsplash](https://unsplash.com/?utm_source=ghost&utm_medium=referral&utm_campaign=api-credit)

Este artículo asume que ya conoces los pasos para contribuir a un proyecto de código abierto. Si no los conoces, quizás te gustaría leer  [este artículo escrito por Maryna](https://rubygarage.org/blog/how-contribute-to-open-source-projects). También asumimos que tienes instalado Git en tu computadora, Si no lo tienes, quizas quieras revisar  [instalación de Git en este artículo](https://docs.github.com/en/github/getting-started-with-github/set-up-git)  y hacerlo antes.

# Paso 1: Fork del proyecto

Esto es tan simple como hacer click en un botón de GitHub. Navega al repositorio del proyecto que desees contribuir, luego haz click en el botón  `fork`  en la parte superior izquierda como se puede observar en la siguiente imagen.

![3](https://www.freecodecamp.org/espanol/news/content/images/2021/05/3.png)

Luego de usar el botón  `fork`  tendrás el repositorio en tu cuenta de GitHub.

# Paso 2: Clonar el proyecto en tu máquina local

Esta es la parte más simple de Git. Navega hasta el repositorio  `forked`  (El repositorio ahora se encuentra en tu lista de proyectos en GitHub). Luego del paso 1 y 2 como puedes ver en la imagen siguiente debes copiar la ruta url clonar el repositorio. Esta url debe verse:  `https:github.com/suretrust.com/freeCodeCamp.git`

![4](https://www.freecodecamp.org/espanol/news/content/images/2021/05/4.png)

Luego debes clonar el proyecto con el comando  `git clone <la url copiada>`  en la linea de comandos como en el siguiente ejemplo:

`git clone https://github.com/suretrust/freeCodeCamp.git`

# Paso 3: Crea upstream

Upstream es necesario para mantener el seguimiento desde tu repositorio al repositorio del proyecto original. Esto es muy útil si deseas contribuir a un repositorio popular.

Algunos repositorios aceptan los  `pull request`  cada hora o menos, así que debes asegurarte que tu  `rama`  tiene los ultimos cambios del repositorio original.

**Debes tener en cuenta que upstream apunta al repositorio freeCodeCamp y no a tu repositorio.**  Siguiendo los pasos 1 y 2 debes copiar la url de upstream.

![5](https://www.freecodecamp.org/espanol/news/content/images/2021/05/5.png)

Para crear un link al repositorio original, copia y pega el siguiente comando en tu terminal:

`git remote add upstream <upstream address>`

Puedes usar  `git pull upstream master`  para confirmar que no ha habido ningún cambio hasta este momento (desde que realizamos el fork del repositorio hasta ahora)-

# Paso 4: Crea la rama dónde vas a trabajar

![6](https://www.freecodecamp.org/espanol/news/content/images/2021/05/6.png)

Photo by  [Zach Reiner](https://unsplash.com/@_zachreiner_?utm_source=ghost&utm_medium=referral&utm_campaign=api-credit)  /  [Unsplash](https://unsplash.com/?utm_source=ghost&utm_medium=referral&utm_campaign=api-credit)

Es bueno crear una nueva rama cada vez que quieras contribuir, esto nos permite identificar que la rama es para la contribución que se está a punto de hacer, podría ser tan pequeño como corregir un error tipográfico o tan largo como la implementación de una nueva funcionalidad. De cualquier manera, es buena práctica crear una rama.

Otra parte importante de la creación de ramas es el nombrado, es agradable usar un nombre que un extraño que no sabe nada del repositorio pueda entender fácilmente. Si quieres añadir una funcionalidad de inicio de sesión, por ejemplo, debes crear una rama llamado  `add-login-feature`  o  `login-feature`.

Para crear una rama debes escribir el siguiente comando en tu terminal:

`git checkout -b <el nombre de tu rama>`

Este comando creará una rama y apuntará a ella, si el nombre de la rama es  `login-feature`  entonces puedes usar el siguiente comando:

`git checkout -b login-feature`

**Añade tu contribución y después muévete al paso 5.**

# Paso 5: Git add y hacer commit de tu contribución

Esto también es bastante simple. Puedes hacer`stage`  y  `commit`  de tus cambios escribiendo lo siguiente en la terminal:

```
// Para hacer stage de los cambios
git add .

//Para hacer commit de los cambios
git commit -m 'Mensaje del commit'

```

Ahora ya has realizado tu commit, ¿Cúal es el siguiente paso?

# Paso 6: Hacer Pull desde upstream a nuestra rama local

Como lo vimos en el paso 4, este paso es mezclar cualquier diferencia en upstream en nuestra local para prevenir conflictos.

`git pull upstream <nombre-de-rama>`

Esto mezcla los cambios de upstream en nuestra rama actual.

# Paso 7: Push de la rama en la que estamos trabajando

Ahora, casi estás ahí.  
Para hacer push de los cambios en los que has estado trabajando debes ejecutar:

`git push origin <nombre-de-rama>`

# Paso 8: Crear un pull request

Este es el paso final para cualquier contribución a un proyecto abierto, estaras diciendo "He realizado algunos cambios, ¿Le importaría agregarlos al proyecto?".

Al abrir una solicitud de pull request, esperaras que el propietario del proyecto o los miembros les guste lo que ven y los mezclen. De lo contrario, podrían realizar cambios o solicitar que tu los realices antes de hacer la mezcla con la rama estable del proyecto.

Para abrir un pull request, navega hasta el repositorio principal como puedes ver en la siguiente imagen. Podrás ver la última rama que subiste 'login-feature', entonces debes hacer click en  `'compare and pull request'`.

![7](https://www.freecodecamp.org/espanol/news/content/images/2021/05/7.png)

Explica claramente los cambios que has realizado y luego crea el  `pull request`  como puedes verlo en la imágen:

![8](https://www.freecodecamp.org/espanol/news/content/images/2021/05/8.png)

Esto es todo. Ahora puedes ir y contribuir a un proyecto ¡como todo un profesional!

# Hoja de comando de Git para contribuir a un proyecto

![9](https://www.freecodecamp.org/espanol/news/content/images/2021/05/9.png)

¡Hasta luego y feliz contribución!
