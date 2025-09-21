# IAdV
Práctica grupo 1.3 de la asignatura de IA para el desarrollo de Juegos 2024/2025.
* David Valera López @dac012
* Pablo Pérez Melgarejo @pablo-perez-melgarejo-um-es
* Frank Antonio Oldfield Montilla @frankoldfield

## Flow de trabajo con git :computer:
Disponemos de dos ramas principales, <ins>**main**</ins>, donde se encontrará la <ins>última versión estable del proyecto</ins> y <ins>**dev**</ins>, la rama de desarrollo donde se irán implementando <ins>funciones de las que no estamos seguros al 100%</ins>. Cada vez que un bloque de trabajo/funcionalidad se haya completado en la rama dev y esta no genere conflictos/bugs, se hará merge desde dev hacia main.

### Creación y resolución de issues
Cada vez que se quiera implementar una nueva funcionalidad o modificar un script preexistente se debe crear un issue y resolverla, siguiendo los siguientes pasos:
1. Crear la issue y posibles sub-issues en [IAdV/Issues](https://github.com/frankoldfield/IAdV/issues).
1. Crear rama en local: ``` git checkout -b [#issue-number]/issue-title``` donde #issue-number es el número de la issue e issue-title es el título de la issue, en minúsculas y separado por guiones.
2. Subir esa rama al repositorio remoto: ``` git push -u origin [#issue-number/issue-title]```
3. Una vez se hayan terminado de resolver esa issue con todos los commits pusheados a remoto, se inicia una pull request.
4. Para resolver la pull request, revisamos los posibles conflictos, si vemos que hay alguno dudoso consultamos con los compañeros antes de hacer nada
5. En la descripción del merge de la pull request poner: ```Closes #[issue-number]``` para que la issue sea resuelta de forma automática
6. Una vez hecho el merge de forma exitosa borrar la rama tanto en remoto como en local

### Resolución de conflictos en una misma rama
En caso de que fuesemos a hacer push o pull y hubiese conflictos, esto se deberá a que nuestra rama está desactualizada, tendremos que hacer lo siguiente:
1. Guardar nuestros cambios en una pila separada y volver a la última versión común a la rama remota: ``` git stash```
2. Hacer pull para sincronizar a la última versión de la rama remota: ``` git pull```
3. Poner nuestros cambios sobre esta última versión: ``` git stash pop```
4. Aquí es posible que haya conflictos y tengamos que elegir con qué fichero nos quedamos ``` git add [#fichero] //para la versión del stash```, ``` git restore [#fichero] //para la versión de la rama``` o solucionar los conflictos a mano
5. Una vez solucionados los conflictos hacemos staging, commit y push (en el commit intentar describir los conflictos que había y cómo se han solucionado, por si mas adelante diesen problemas y se tuviese que deshacer algún commit)

>[!CAUTION]
> Cuando queramos trabajar sobre un fichero que puede afectar a otras funcionalidades, aunque sea para comentarlo o para hacer refactoring sobre el código, avisar a los compañeros, por si alguien ya estuviese trabajando sobre ese fichero en otra rama, o por si el refactoring pudiese afectar a código todavía no mergeado.

>[!WARNING]
>Métodos peligrosos! (mirar pdf práctica antes de usar)
>* Transform.forward
>* Transform.Translate
>* Transform.Rotation()
>* Transform.LookAt()
>* Mathf.Lerp()
