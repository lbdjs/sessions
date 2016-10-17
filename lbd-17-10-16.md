# Learning by doing - Babel

- [Babel](https://babeljs.io/) is a JavaScript compiler
- Babel transforms your JavaScript

### Exercise
1- Crear un nuevo repositorio en [GitHub](https://github.com/) llamado lbd-17-10-16   

2- Clonar el repo en local `$ git clone xxx`  

3- Crear un [package.json](https://docs.npmjs.com/files/package.json) con `$ npm init -f`   

4- Añadir Babel e [instalarlo](https://babeljs.io/docs/setup/#installation) en local:   
`$ npm install --save-dev babel-cli`   

```javascript  
...
"devDependencies": {
    "babel-cli": "^6.0.0"
  }
...
```
5- Añadir el paquete Babel ES2015  
`$ npm install babel-preset-es2015 --save-dev`  

6- Create `.babelrc` configuration file y añadir ES 2015   
```javascript
{
  "presets": ["es2015"]
}
```
7- [Como usarlo  ](https://babeljs.io/docs/usage/cli/)  

Files:  
If you would like to output to a file you may use --out-file or -o.   

`$ babel script.js --out-file script-compiled.js`   

Folders:   
Compile the entire src directory and output it to the lib directory. You may use --out-dir or -d.   

`$ babel src --out-dir lib`   


Acceder directamente a `babel` local:   
`$ ./node_modules/.bin/babel src -d lib`  

8- package.json "scripts"   

```javascript
"scripts": {
  "build": "babel src -d lib -w"
},
```

Folder structure
```
|- src 
    |- index.html
    |- app.js
|- lib 
    |- * //El conteindo se generará con babeljs
|- node_modules/
    |- ...
|- package.json
|- .babelrc
|- .gitignore (node_modules/)  
```

9- Atom live server  
Instalar [atom live server](https://atom.io/packages/atom-live-server) para correr la aplicación

10- Escribir algún código ES6   


11- Subir los cambios a GitHub  

##### Fuente
- https://docs.npmjs.com/cli/init
- https://docs.npmjs.com/files/package.json
- https://babeljs.io/
