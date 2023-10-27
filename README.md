# examenDAM
Para utilizarlo en el examen

# Comandos de el examen
Antes de empezar el ejercicio1 tengo que clonar mi fork para poder trabajar con el
```
git clone https://github.com/mpineirotroncoso/examenCOD_Parte2
```

1. 
Copio los contenidos de la carpeta del proyecto en la carpeta del examen
añado la carpeta src con todos sus archivos
```
git add src/
```
hago commit
```
git commit -m "ejercicio1"
```
hago push con mis cambios, como el repositorio original usaba la rama master yo segui usandola, si quisiera cambiarla a la main usaría `git branch -M main`
```
git push -u origin master
```
2. 
Creo un gitignore con `nano .gitignore` y escribo las rutas de archivos y carpetas que no quiero hacer un seguimiento
```
out/
# carpeta de salida que usa el intellij
.idea/
# carpeta del intellij
Primero.iml
# archivo que especifica los modulos que necesita el programa
```
3. 
En intellij voy a `Project Structure > artifacts` y le doy al `+`. Pulso en `jar > From modules with dependencies`
selecciono la `Main class` con la `Main` de mi proyecto y le doy todo a ok.

En el menu superior busco `build` y pulso en `Build artifacts`, pulsamos en el artifact que creamos antes y le damos a build.

El artifact por defecto se crea en la carpeta `out/artifacts/Primero_jar/`, nos desplazaremos alli con `cd`y lo ejecutaremos con
```
java -jar Primero_jar
```
4. 
Tenemos que modificar nuestro `.gitignore` para poder hacer un control sobre nuestro artefacto que se encuentra en la carpeta `out`
```
# editamos el out, especificamos que solo ignore la carpeta production
out/production/
.idea/
Primero.iml
```
Añadimos nuestro artifact en git
```
git add out/artifacts/Primero_jar/Primero.jar
```
Hacemos un commit
```
git commit -m "añadido artifact"
```
Hacemos un push a nuestro repositorio
```
git push -u origin master
```
