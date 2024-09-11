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
por lo que se tiene que hacer un cambio en el archivo vite.config.js

export default defineConfig({
  plugins: [react()],
  server: {
    proxy: {
      '/api': {
        target: 'http://localhost:3001',
        changeOrigin: true
      }
    }
  }
})

siempre y cuando la baseUrl sea igual a 
  const baseURL='/api/notes'


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

