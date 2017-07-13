### git tag nombre-etiqueta
Lista las etiquetas en orden alfabético.

### git tag -a nombre-etiqueta -m "mensaje"
Etiqueta anotada. Se guarda en la base de datos Git como un objeto entero. Tiene un checksum; contieneel nombre del etiquetador, correo y fecha; y tiene un mensaje asociado.

```
git tag -l "v1.*"
```
Lista las etiquetas que coincidan según el patrón