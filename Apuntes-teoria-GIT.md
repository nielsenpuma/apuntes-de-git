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

--Ver las diferencias del archivo modificado
git diff
git diff --staged (Cuando se modifica un archivo en la zona de preparación, es bueno ver los cambios, de acuerdo a eso hacer los commits necesarios)

(Siempre es bueno con "git status" ver que el directorio de trabajo esté limpio -> working tree clean)

-- Sacar un archivo de la zona de preparación.
git reset HEAD <tuarchivo> (Vuelve el archivo a la zona de directorio de trabajo)

-- Si se equivoca en el mensaje de un commit
git commit --amend (Preferencia con editor VIM para modificar)

-- Para ignorar archivos .gitignore
1. Se crea el archivo .gitignore
2. Dentro de agregan los archivos a ser ignorados y no les tomará en cuenta al momento del ADD o COMMIT