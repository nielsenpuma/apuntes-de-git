### git log
Muestra el historial de commit del proyecto

`git log --pretty=format:"%h - %an, %ar : %s"`
Muestra el historial en el formato que indicamos.

### Limitar la salida del historial
`git log -n`: cambiamos la n por cualquier número entero, por ejemplo: `git log -2` commits más recientes.

`git log --after="2016.01-07 00:00:00"`: Muestra los commit realizados después de la fecha específica.

`git log --before="2016.01-07 00:00:00"`: Muestra los commit realizados antes de la fecha específicada.

Las banderas del comando `git log`se pueden usar juntas según convenga, por ejemplo: `git log --after="2016.01-07 00:00:00" --before="2016.01-07 00:00:00"`