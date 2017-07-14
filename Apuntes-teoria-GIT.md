-- Configuración de GIT
git config --global user.name "Nielsen Puma"
git config --global user.email "nielhpuma@gmail.com"

-- Verificar Configuración
git config user.name
git config user.email

--Configurar editor para Git
git config --global core.editor code
-- Verificar configuración de editor
git config core.editor

-- Listar las configuraciones del usuario
git config --list | grep user
git config --list | grep editor
-- Listar todas las configuraciones
git config --list

--Solicitar ayuda
git <comando> --help
VS Code el comando que lo lanza es "code --wait"

--Iniciar el repositorio una vez ubicado en la carpeta del proyecto
git init

--Ver estatus de git (cuando se comenzó con el proyecto)
git status (indica ayuda de lo que pueda faltar en rojo)

--Primer commit (Pasa al área de preparación)
git add <tuarchivo_rojo> 
git add . (Agrega todos los archivos estén o no estén confirmados a la zona de preparación)
git add -A (Agrega solo los achivos que estén confirmado en la zona de preperación. RECOMENDADO)

--Confirmar commit (Zona del repositorio, se inicia la linea del tiempo)
git commit -m "Primer commit"

--Ver los commits en la línea de tiempo
git log
git log --oneline (muestra todos los commit en una sola linea)
git log --oneline --graph (gráficamente muestras las ramas)
git log -2 (muestra los dos últimos commit)
git log --pretty=format:"%h - %an, %ar : %s" (formato personalizado el mostrar los commit)
git log  --before="2017-07-12 15:00:00" (Muestra los commit antes de <fecha>)
git log  --after="2017-07-12 13:00:00" (Muestra los commit después de <fecha>)
git log  --after="2017-07-12 13:00:00" --before="2017-07-12 15:00:00" (Muestra commits dentro del rango)

--Ver las diferencias del archivo modificado
git diff
git diff --staged (Cuando se modifica un archivo en la zona de preparación, es bueno ver los cambios, de acuerdo a eso hacer los commits necesarios)
git diff <idcommit> <idcommit> (sirve para ver las diferencias entre un commit y otro)

(Siempre es bueno con "git status" ver que el directorio de trabajo esté limpio -> working tree clean)

-- Sacar un archivo de la zona de preparación.
git reset HEAD <tuarchivo> (Vuelve el archivo a la zona de directorio de trabajo)
Cuando quieres sacar un archivo(s) de la zona de preparación.

-- Si se equivoca en el mensaje de un commit
git commit --amend (Preferencia con editor VIM para modificar, reace la confirmación o commit)

Este comando utiliza el área de preparación para la confirmación. Al final terminarás con una sola confirmación - la segunda confirmación reemplaza al resultado de la primera.

Si no hemos hecjo cambios desde la última confirmación, entonces la instantánea o el commit lucirá exactamente igual y lo único que cambiaremos el mensaje del commit.

-- Para ignorar archivos .gitignore
1. Se crea el archivo .gitignore
2. Dentro de agregan los archivos a ser ignorados y no les tomará en cuenta al momento del ADD o COMMIT

-- Elimina archivos
git rm (Elimina definitivamente del historial de git)

-- Restaurar un fichero eliminado por software
git checkout <tuarhivo>
también sirve para moverse dentre de la historia, ejemplo:
git checkout 7d72503, donde los números es el hash de los commit (el pasado)
git checkout master -> Regresando al presente.
git checkout -b <turama> -> Permite crear la rama anterior, siempre y cuando estemos ubicados en hash de la supuesta rama.

-- Renombrar los archivos
git mv <tuarchivo> <nuevonombre>

-- Descartar un archivo modificado (deshacer)
git checkout -- <file>

-- Etiquetar un commit
git tag (lista las etiquetas generadas)
git tag mi-etiqueta (agrega una etiqueta al último commit)
git tag mi-etiqueta 86dec27 (coloca una etiqueta en un punto de la historia)
git tag -d <mi-etiqueta> Eliminamos una etiqueta

-- Etiqueta anotada (Se guardan en la base de datos de Git como objetos enteros)
git tag -a v1.0 -m "tumensaje"

-- Ver el detalle del commit según la etiqueta
git show <mietiqueta>

-- Crear nuevas ramas.
git branch (lista las ramas y con * la rama actual donde estamos)
git branch -v (Lista las últimos commit de todas las ramas)
git branch <tunuevarama> (se crea la nueva rama en el commit actual)

-- Fusiones de ramas con la principal
git merge <nombre-rama> (fusiona una rama con la rama actual)

--Eliminar una rama si ya ha sido fusionada
git branch -d <nombre-rama>
git branch -D <nombre-rama> (Elimina una rama esté o no esté fusionada. OJO)
git branch --no-merged (lista ramas que no han sido fusionadas a la rama actual)
git branch --merged (lista las ramas que han sido fusionadas)