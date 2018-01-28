## Probando librerias
El objetivo es instalar la libreria babel y gitignore

## Pasos
1. Ubicarte en la carpeta de inicialización

2. Ejecutar en el gitbush `npm init`, aparecerá el archivo `package.json`.Al ejecutarlo aparecere una serie de preguntas o items que se debe de modificar pero lo puedes obviar con enter ya que se puede  modificar después en el editor.
Nota: En este archivo en la parte de scripts se debe de borrar  `"test": "echo \"Error: no test specified\" && exit 1"` y se debe de poner   `"build": "babel src -d lib"`.

3. Ejecutar en el gitbush `npm install --save-dev babel-cli babel-preset-env`, el resultado es que aparece el archivo `package-lock.json` y el archivo `node_modules`

4. Crear manualmente el archivo  `.babelrc` e incorporar en ese archivo lo siguiente:
{
  "presets": ["env"]
}

5. Luego crear también manualmente el archivo `.gitignore` para que git, ciertos archivos los ignore y no los subas como por ejemplo el `node_modules`. En este archivo se debe de escribir los archivos que no se desean subir.Se incorpora lo siguiente:

`node_modules/

.DS_Store

Thumbs.db `

Se elimina lo siguiente:

-.DS_Store: Archivos en una MAC
-Thumbs.db: Archivos que actuan como caché en windows.

Finalmente se puede subir todos los archivos a la plataforma `github`.

* Nota: Es necesario incorporar el gitignore para que no se suba a la plataforma el modulo node_modules ya que posees muchos archivos.
