se va a crear un repositorio en github 
en el repositorio se van a guadar dos carpetas backend y frontend
en el frontend se tiene que hacer 
     npm run deploy
que crea la carpeta dist, 
se copia esa carpeta y se pega en la carpeta backend
en el archivo index del backend se tiene que agregar un middleware
    app.use(express.static('dist'))

al momento de hacer el primer deploy no se ejecutara la parte de las notas porque 
el baseUrel se tiene que modificar con la direccion de las notas que nos de render
esta se obtiene despues de hacer el primer deploy una vez obtenida la direccion de las notas
se copia y se pega en la baseUrl del frontend.
luego en la pagina de render
    new
        web service
            conectar a git hub (buscar el repositorio del proyecto, tiene dos carpetas backend y frontend)
 
 va a desplegar una lista que hay que llenar y ver bien si hay que modificar los siguientes espacios
    language:node
    Root Directory: se pone el nombre de la carpeta que contiene el backend
    Build command: npm install (esto en caso de que se cuente con un package.json)
    start command: npm start

y presionar el boton de abajo 
    deploy web service
        
se agregan unas lineas al script de package.json del backend 

