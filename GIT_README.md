# Comandos Git y Github

Terminal :
- Para salir de una rama: `git checkout main`

- Para crear una nueva rama: `git checkout -b dev` 
- Para crear un file: `touch index.js`
- Para ver que archivos tenemos: `ls`
- Para agregar todo los cambios: `git add .`
- Para agregar cambios de un file específico: `git add index.js`
- Para subir los cambios a una rama: `git push origin dev`  .

<br>

# Pull Request:
Un pull request es cuando se hace el merge entre dos ramas, en este caso la rama principal (main) con otra rama.

Para que los cambios  realizados en github se visualicen en nuestra carpeta local:
```bash
$ git pull origin main
```  

Para ver el estado de nuestro repositorio y si tiene algun cambio:
```bash
$ git status
``` 

Para ver un historial de los commits creados:
```bash
$ git log
``` 

Para crear una etiqueta o version del proyecto:
```bash
$ git tag v1.0
``` 

Para subirlo a github:
- `git push --tags` o  `git push origin v1.0`

<br>

# Comandos avanzados para multiples entornos
Cuando un miembro del equipo realizo algun cambio en el repositorio y quieres cargar los que has hecho. Primero debes realizar lo siguiente:

Para limpiar:
```bash
$ git stash clear
```

Para guardar todo los cambios de manera temporal en tu carpeta local:
```bash
$ git stash save "Mensaje"
```

Para traer todo los cambios del repositorio de gitHub a nuestra carpeta local:
```bash
$ git pull origin main
```
Para que se integren los cambios que habias realizado:
```bash
$ git stash pop
```
Para sacar lo que estaba al inicio de la pila:
```bash
$ git stash pop s init
```
<br>

# Modificar un Commit
Si queremos modificar el mensaje de un commit, podemos hacer lo siguiente:
```bash
$ git commit --amend -m "texto"
```
Esto nos permitira editar el ultimo commit con el texto especificado.

<br>

----------------------------------------------------------------

# Confictos en GIT:
Cuando dos usuarios trabajan sobre el mismo archivo y hagamos alguna modificación sin tener cuidado no podremos realizar commit. Para solucionar este conficto hacemos lo siguiente:

- Manualmente eliminar las líneas de código que no se necesitan y git commit.

`git checkout`: Saber cuál de los cambios conservar (rama padre - main) o rama hija
`git checkout --ours`  - padre <br>
`git checkout -- theirs` - hija
<br>



<br>

# Comandos Avanzados Para Emergencias
En caso de emergencia, puedes revertir los cambios hacia un commit anterior. Tambien podemos deshacer esta accion.
Este comando permite volver al pasado (revertir) cualquier commit.
```bash
$ git revert
```
Ejemplos de <`git rever "codigo" `>:
- Suponiendo que nuestro commit actual es el `7b63ead`

Especificamos el codigo del commit a revertir o regresar 
```bash
$ git revert 6b63ead
```

Si quieres revertir esta accion y regresar a la version que tenias debes usar el codigo del commit anterior
```bash
$ git revert 7b63ead
```

Para ver la lista de commits ordenada:
```bash
$ git log --online
```
<br>

# Reglas para crear un historial de Commits:
1.- Los mensajes deben ser cortos pero significativos.<br><br>
2.- No pongas mas de una sola cosa por cada commit.<br><br>
3.- Si estuviste trabajando en algo diferente desde antes, no te olvides de comitearlo.<br><br>
4.- Evita tener muchos commits pequeños.<br><br>
5.- Cuando termines tu trabajo, ejecuta `$ git push`. Esto enviará tus cambios a GitHub.<br>

Los commit nos sirven para comunicar la naturaleza de los cambios a las personas que trabajan o desean ver el proyecto:

#Ejemplo de estructura:
- A) Feat= `"add amazing button"`  
- B) Build=`"add version to 1.2.0"` 
- C) Feat=` "add component button"` 


- Build (release): se refiere a los lanzamientos de nuestra aplicación.<br>

<br>

Lista de algunas:


Buil:
- lanzamiento de compilación.<br>

Feat:
- Nuevas funcionalidades
- Corrección de errores
- Mejoras funcionales
- Inclusión de nuevos elementos.


Fix (bug): cuando corregimos algún bug.
- Corregido error
- Solucionado problema
- Arreglado falta.


Docs:
- Documentación


Style:
- Formato CSS


Refactor:
- Refactorización


Test:
- Prueba unitaria


Chore:
- Tareas menores


Merge:
- Fusionar ramificaciones


Revert:
- Descarte o reversión

<br>

# Ramas
Las ramas `master` o `main` se crean por defecto por tanto son las ramas principales. <br>
La rama developer `dev` es la rama de desarrollo.

Algunos tipo de Ramas son:
- `Feature`: Hace referencia a una nueva funcionalidad.
- `Hotfix`: Hace referencia a la rama de correccion de la rama principal.

- `Release`: Hace referencia al lanzamiento del proyecto en producción, esto puede ser un tag o branch. Tambien sirve para estandarizar o acortar una linea de desarrollo se `merchea` y `depura`

--------------------------------------------------------
# Ramas II
git switch -c  `<nombre de la Rama>` para crear
git switch  `<nombre de la Rama>` cambia nuesta area de trabajo a una nueva rama  <br>
git branch <br>

Se debe crear una nueva rama cada que se realice un cambio importante en nuestro codigo


