# Documentación del proyecto

## Estructura de Carpetas:
1. **frontend** - Contiene el código fuente del frontend desarrollado con Angular. Esta carpeta se organiza de la siguiente manera:
   - **src**: Contiene los archivos fuente de la aplicación Angular, incluyendo componentes, servicios, estilos, imágenes, y otros recursos.
   - **assets**: Almacena los archivos estáticos como imágenes, iconos, archivos de configuración, etc.
   - **app**: Contiene los componentes principales de la aplicación, como los componentes de inicio de sesión, registro, página de inicio, etc.
   - **services**: Incluye los servicios de Angular utilizados para interactuar con la API del backend y realizar operaciones CRUD.

2. **backend** - Contiene el código fuente del backend desarrollado con Laravel. Esta carpeta se organiza de la siguiente manera:
   - **app**: Contiene los modelos, controladores, middleware y otros componentes de la aplicación Laravel.
   - **config**: Almacena los archivos de configuración de Laravel, como las configuraciones de la base de datos, autenticación, etc.
   - **database**: Contiene las migraciones de la base de datos y las semillas de datos iniciales.
   - **routes**: Incluye los archivos de rutas de la aplicación, donde se definen las URL y los controladores correspondientes.

3. **docs** - Carpeta destinada a almacenar la documentación relacionada con la aplicación. Esta carpeta puede tener subcarpetas que agrupen diferentes tipos de documentos, como manuales, diagramas, ejemplos de código, etc.

## Instalación y Configuración:
1. **Requisitos del Sistema**:
   - Node.js: Versión X.X.X o superior. Puedes descargarlo desde [https://nodejs.org/].
   - Angular CLI: Versión X.X.X o superior. Puedes instalarlo globalmente ejecutando `npm install -g @angular/cli`.
   - PHP: Versión X.X.X o superior. Puedes descargarlo desde [https://www.php.net/].
   - Composer: Versión X.X.X o superior. Puedes descargarlo desde [https://getcomposer.org/].
   - Laravel: Versión X.X.X o superior. Puedes instalarlo ejecutando `composer global require laravel/installer`.

2. **Configuración del Entorno de Desarrollo**:
   - Clonación del Repositorio: Clona el repositorio desde [URL del repositorio] ejecutando `git clone <URL>`.
   - Instalación de Dependencias Frontend: Navega a la carpeta "frontend" y ejecuta `npm install` para instalar las dependencias del frontend.
   - Instalación de Dependencias Backend: Navega a la carpeta "backend" y ejecuta `composer install` para instalar las dependencias del backend.
   - Configuración del archivo `.env`: Duplica el archivo `.env.example` en la carpeta "backend", renómbralo como `.env` y configura las variables de entorno necesarias, como las credenciales de la base de datos y otras configuraciones específicas.

3. **Ejecución de la Aplicación**:
   - Servidor de Desarrollo Frontend: Inicia el servidor de desarrollo del frontend

 con el comando `ng serve` en la carpeta "frontend".
   - Servidor de Desarrollo Backend: Inicia el servidor de desarrollo del backend con el comando `php artisan serve` en la carpeta "backend".

## Funcionalidades Principales:
La aplicación ofrece las siguientes funcionalidades principales:

1. **Autenticación y Autorización**:
   - Registro de Usuario: Permite a los usuarios crear una cuenta en la aplicación.
   - Inicio de Sesión: Permite a los usuarios iniciar sesión utilizando sus credenciales.
   - Cierre de Sesión: Permite a los usuarios cerrar sesión y finalizar su sesión activa.

   **Ejemplo de Petición de Registro**:
   ```json
   POST /api/auth/register
   Content-Type: application/json

   {
     "name": "John Doe",
     "email": "johndoe@example.com",
     "password": "mypassword"
   }
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 200 OK
   Content-Type: application/json

   {
     "message": "User registered successfully"
   }
   ```

2. **Gestión de Rutinas de Ejercicio**:
   - Obtener Rutinas: Permite a los usuarios obtener una lista de sus rutinas de ejercicio.
   - Crear Rutina: Permite a los usuarios crear una nueva rutina de ejercicio.
   - Actualizar Rutina: Permite a los usuarios actualizar una rutina existente.
   - Eliminar Rutina: Permite a los usuarios eliminar una rutina existente.

   **Ejemplo de Petición para Crear una Rutina**:
   ```json
   POST /api/routines
   Content-Type: application/json
   Authorization: Bearer <token>

   {
     "name": "Rutina de Fuerza",
     "description": "Rutina de ejercicios para ganar fuerza",
     "exercises": [
       {
         "name": "Press de Banca",
         "sets": 3,
         "reps": 8,
         "weight": 100
       },
       {
         "name": "Sentadillas",
         "sets": 3,
         "reps": 10,
         "weight": 120
       }
     ]
   }
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 201 Created
   Content-Type: application/json

   {
     "id": 1,
     "name": "Rutina de Fuerza",
     "description": "Rutina de ejercicios para ganar fuerza",
     "exercises": [
       {
         "id": 1,
         "name": "Press de Banca",
         "sets": 3,
         "reps": 8,
         "weight": 100
       },
       {
         "id": 2,
         "name": "Sentadillas",
         "sets": 3,
         "reps": 10,
         "weight": 120
       }
     ]
   }
   ```

3. **Gestión de Ejercicios**:
   - Obtener Ejercicios: Permite a los usuarios obtener una lista de todos los ejercicios disponibles.
   - Crear Ejercicio: Permite a los usuarios crear un nuevo ejercicio.
   - Actualizar Ejercicio: Permite a los usuarios actualizar un ejercicio existente.
   - Eliminar Ejercicio: Permite a los usuarios eliminar un ejercicio existente.

   **Ejemplo de Petición para Crear un Ejercicio**:
   ```json
   POST /api/exercises
   Content-Type: application/json
   Authorization: Bearer <token>

   {
     "name": "Press de Hombros",
     "description": "Ejercicio para fortalecer los hombros",
     "videoUrl": "https://www.youtube.com/watch?v=123456"
   }
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 201 Created
   Content-Type: application/json

   {
     "id": 3,
     "name": "Press de Hombros",
     "description": "Ejercicio para fortalecer los hombros",
     "videoUrl": "https://www.youtube.com/watch?v=123456"
   }
   ```

4. **Seguimiento de Progreso**:
   - Obtener Progreso: Permite a los usuarios obtener su historial de progresos para un ejercicio específico.
   - Agregar Progreso: Permite a los usuarios agregar un nuevo registro de progreso para un ejercicio específico.

   **Ejemplo de Petición para Agregar Progreso**:
   ```json
   POST /api/progress/1
   Content-Type: application/json
   Authorization: Bearer <token>

   {
     "weight": 105,
     "reps": 8,
     "date": "2023-06-13"
   }
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 201 Created
   Content-Type: application/json

   {
     "id": 4,
     "exerciseId": 1,
     "weight": 105,
     "reps": 8,
     "date": "2023-06-13"
   }
   ```

5. **Gestión de Comidas**:
   - Obtener Comidas: Permite a los usuarios obtener una lista de todas las comidas registradas.
   - Crear Comida: Permite a los usuarios crear una nueva comida.
   - Actualizar Comida: Permite a los usuarios actualizar una comida existente.
   - Eliminar Comida: Permite a los usuarios eliminar una comida existente.

   **Ejemplo de Petición para Crear una Comida**:
   ```json
   POST /api/meals
   Content-Type: application/json
   Authorization: Bearer <token>

   {
     "name": "Desayuno",
     "description": "Comida para el desayuno",
     "calories": 300
   }
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 201 Created
   Content-Type: application/json

   {
     "id": 2,
     "name": "Desayuno",
     "description": "Comida para el desayuno",
     "calories": 300
   }
   ```

6. **Interacciones Sociales**:
   La sección de Reels permite a los usuarios compartir fotos y videos relacionados con su experiencia en el gimnasio. Los usuarios pueden subir sus propias fotos y videos, y también pueden explorar contenido de otros usuarios de forma aleatoria.

   **Ejemplo de Petición para Subir un Reel**:
   ```json
   POST /api/social/reels
   Content-Type: multipart/form-data
   Authorization: Bearer <token>

   [archivo de imagen/video adjunto]
   ```

   **Respuesta del Servidor**:
   ```json
   Status: 201 Created
   Content-Type: application/json

   {
     "id": 1,
     "userId": 1,
     "mediaUrl": "https://example.com/reels/1",


     "timestamp": "2023-06-13T10:00:00Z"
   }
   ```
