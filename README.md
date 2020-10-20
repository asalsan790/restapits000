# Primer paso creación del servidor
Herramientas:

nodejs
typescript
mongodb

Luego, en la carpeta del proyecto:
npm init
npm install -g typescript
tsc --init
git init

Cambiamos en tsconfig.ts:

"target": "es6",  
"outDir": "./build",	

npm i express mongoose morgan helmet cors compression

helmet de seguridad los otros no son muy importantes

Creamos la carpeta src con server.ts

npm install @types/node @types/mongoose @types/express @types/cors @types/compression @types/morgan nodemon typescript -D

Configuramos el .gitignore con:
build
node_modules

Hay que compilar con:
 tsc  y 
 ejecutaremos con:
node build/server.js

Observar el package.json con:

  "scripts": {
    "ts": "tsc -w",
    "dev": "nodemon ./build/server.js",
    "start": "tsc && ./build/server.js"
  },

Y podemos ejecutar con:
El compilador:
npm run ts

El Servidor:
npm run dev

El “start” será para producción:
(Quizás no será necesario el tsc &&)

npm start


