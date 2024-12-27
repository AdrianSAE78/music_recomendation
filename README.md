# Proyecto de Música con Node.js y Frontend en HTML, CSS y JavaScript

Este proyecto consiste en una aplicación de música donde se pueden recomendar y subir canciones utilizando un backend desarrollado con Node.js y Express, y un frontend con HTML, CSS y JavaScript. El backend se conecta a una base de datos MongoDB para almacenar la información de las canciones.

## Estructura del Proyecto

El proyecto sigue el patrón de arquitectura MVC (Modelo-Vista-Controlador). El backend (Node.js) se encarga de la lógica y las interacciones con la base de datos, mientras que el frontend (HTML, CSS, JavaScript) se encarga de la interfaz de usuario.

### Backend
- **Node.js**: Usado como entorno de ejecución.
- **Express**: Framework para la creación del servidor.
- **MongoDB**: Base de datos NoSQL para almacenar canciones.
- **CORS**: Para permitir que el frontend (en un puerto diferente) pueda hacer solicitudes al backend.

### Frontend
- **HTML**: Estructura de las páginas web.
- **CSS**: Estilo y diseño.
- **JavaScript**: Lógica y interacción del usuario.

## Instrucciones para Ejecutar el Proyecto

### Backend
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
   cd tu-repositorio
2. **Instalar dependencias del backend: Asegúrate de tener Node.js instalado. Luego, ejecuta:**
   ```bash
   npm install
3. **Conectar con la base de datos MongoDB: Asegúrate de tener una instancia de MongoDB corriendo. Si tienes MongoDB localmente, el puerto predeterminado es 27017. Puedes cambiar la URL de conexión en el archivo server.js si usas una base de datos remota.**
4. **Ejecutar el backend: Inicia el servidor con:**
   ```bash
   node server.js
 El servidor backend se ejecutará en el puerto 3000 por defecto:
   ```bash
    Servidor corriendo en el puerto 3000
```
### Frontend
1. **Ejecutar el frontend con Live Server:** El frontend debe ser ejecutado utilizando Live Server en un editor como Visual Studio Code.
- Abre el archivo index.html con Visual Studio Code.
- Haz clic derecho sobre el archivo y selecciona "Open with Live Server".
Esto abrirá el frontend en un puerto como el 5501 (por ejemplo: http://127.0.0.1:5501).

2. **Configurar CORS:** Asegúrate de que el backend permita solicitudes desde el puerto en el que ejecutas el frontend. En el archivo del backend (server.js), configura CORS de la siguiente manera:
   ```bash
   let corsOptions = {
    origin : 'http://127.0.0.1:5501', // Cambia el puerto si usas otro
    optionSuccessStatus: 200
    }
   ```
Esto permite que el frontend en http://127.0.0.1:5501 haga peticiones al backend que está corriendo en el puerto 3000.

** Estructura de Archivos
/music_recomendation
│
├── backend/
│   ├── server.js
│   ├── model/
│   ├── controller/
│   └── view/
│
├── frontend/
│   ├── index.html
│   ├── styles.css
│   └── script.js
│
├── .gitignore
└── README.md

