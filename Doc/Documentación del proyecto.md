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

## Formato de Respuesta del Servidor:
El servidor responderá con un objeto JSON en la mayoría de las solicitudes. El formato de respuesta general será el siguiente:

```json
{
  "success": true,
  "message": "Mensaje de éxito o información adicional",
  "data": { ... } // Contenido de la respuesta específica
}
```

- El campo "success" indicará si la solicitud fue exitosa (true) o si ocurrió algún error (false).
- El campo "message" proporcionará un mensaje descriptivo sobre el resultado de la solicitud.
- El campo "data" contendrá los datos específicos de la respuesta, como un objeto o una matriz.

En caso de errores, el servidor puede devolver una respuesta con un código de estado HTTP correspondiente y un mensaje de error adicional en el campo "error".

## Manejo de Errores:
El servidor manejará los errores de manera adecuada y proporcionará respuestas descriptivas en caso de que ocurra algún problema. Los códigos de estado HTTP y los mensajes de error ayudarán a identificar la naturaleza del error y tomar medidas apropiadas para solucionarlo.

Aquí hay algunos ejemplos de posibles mensajes de error:

- **400 Bad Request**: Se produce cuando la solicitud no es válida debido a datos faltantes o incorrectos. El mensaje de error puede proporcionar más detalles sobre el problema.
- **401 Unauthorized**: Se produce cuando la solicitud requiere autenticación, pero no se proporcionaron credenciales válidas.
- **403 Forbidden**: Se produce cuando la solicitud está prohibida debido a permisos insuficientes.
- **404 Not Found**: Se produce cuando el recurso solicitado no se encuentra en el servidor.
- **500 Internal Server Error**: Se produce cuando ocurre un error interno en el servidor.

Es importante manejar estos errores adecuadamente en el frontend para proporcionar retroalimentación clara al usuario.

## Consideraciones de Seguridad:
- Autenticación y Autorización: Utiliza un sistema de autenticación sólido para proteger las rutas y las funcionalidades sensibles. Implementa un sistema de tokens de acceso (JWT) para permitir a los usuarios autenticados acceder a recursos protegidos.
- Validación de Datos: Valida y filtra todos los datos de entrada para prevenir ataques de inyección y garantizar la integridad de los datos almacenados.
- Protección contra CSRF: Implementa medidas para prevenir ataques de falsificación de solicitudes entre sitios (CSRF) utilizando tokens CSRF en las solicitudes que modifican datos.
- Almacenamiento Seguro de Contraseñas: Almacena las contraseñas de los usuarios de forma segura utilizando técnicas de hashing y salting para proteger la información confidencial.

Por supuesto, aquí tienes más información para completar la documentación:

## Pruebas Unitarias:
Es recomendable escribir pruebas unitarias para verificar el correcto funcionamiento de las diferentes partes de la aplicación. Tanto Angular como Laravel proporcionan herramientas y marcos de pruebas para facilitar este proceso.

- En Angular, puedes utilizar el framework de pruebas integrado (Jasmine) y la herramienta de testing (Karma) para escribir pruebas unitarias para los componentes, servicios y directivas.
- En Laravel, puedes utilizar el framework de pruebas integrado (PHPUnit) para escribir pruebas unitarias para las clases, modelos y controladores.

Es importante cubrir los casos de uso más comunes y los escenarios límite en las pruebas unitarias para garantizar la estabilidad y calidad del código.

## Despliegue y Hosting:
Una vez que hayas completado el desarrollo de la aplicación, deberás considerar cómo desplegarla y alojarla en un entorno de producción. Aquí hay algunas opciones gratuitas para el despliegue y hosting de Angular y Laravel:

- Angular:
  - GitHub Pages: Puedes alojar la parte frontend de tu aplicación en GitHub Pages de forma gratuita. Solo necesitas crear un repositorio en GitHub y seguir las instrucciones para desplegar la aplicación.
  - Netlify: Netlify es una plataforma de alojamiento web gratuita que te permite desplegar fácilmente aplicaciones estáticas de Angular.

- Laravel:
  - Heroku: Heroku ofrece planes gratuitos que permiten desplegar aplicaciones Laravel en su plataforma en la nube.
  - InfinityFree: InfinityFree es un servicio de hosting gratuito que soporta PHP y MySQL, lo cual es adecuado para alojar una aplicación Laravel.

## Guía de Uso

### Crear una Rutina de Ejercicio
1. Inicia sesión en la aplicación utilizando tus credenciales.
2. Navega hasta la sección "Rutinas" en el menú principal.
3. Haz clic en el botón "Crear Rutina".
4. Completa los campos requeridos, como el nombre de la rutina y la descripción.
5. Selecciona los ejercicios que deseas incluir en la rutina y ajusta los detalles, como el número de series y repeticiones.
6. Guarda la rutina y estará disponible en tu perfil para su uso.

### Registrar Progresos
1. Accede a la sección "Progresos" en el menú principal.
2. Busca el ejercicio para el cual deseas registrar un progreso.
3. Haz clic en el botón "Agregar Progreso".
4. Ingresa los detalles de tu progreso, como el peso utilizado, el número de repeticiones y la fecha.
5. Guarda el progreso y se registrará en tu historial personal.

### Explorar Reels y Fotos
1. Dirígete a la sección "Social" en el menú principal.
2. Explora los Reels y fotos recientes de otros usuarios que se muestran de forma aleatoria.
3. Si deseas subir tu propio Reel o foto, haz clic en el botón "Subir" y selecciona el archivo correspondiente.
4. Proporciona una descripción opcional y guarda tu publicación para que otros usuarios puedan verla.

## Preguntas Frecuentes (FAQ)

### ¿Puedo cambiar mi rutina de ejercicio?
Sí, puedes modificar tu rutina de ejercicio en cualquier momento. Navega hasta la sección "Rutinas", selecciona la rutina que deseas cambiar y haz clic en el botón "Editar". Realiza los ajustes necesarios y guarda los cambios.

### ¿Cómo puedo ver mi progreso a lo largo del tiempo?
En la sección "Progresos", podrás ver un historial detallado de tus progresos para cada ejercicio. Utiliza los filtros disponibles para visualizar tu progreso en un período específico o para un ejercicio en particular.

### ¿Puedo eliminar una publicación de Reel o foto?
Sí, tienes la opción de eliminar tus propias publicaciones de Reels o fotos. Simplemente accede a la publicación que deseas eliminar y haz clic en el botón "Eliminar".

## Política de Privacidad

Nuestra aplicación se compromete a proteger la privacidad y seguridad de los datos de los usuarios. A continuación, se presentan algunos puntos importantes de nuestra política de privacidad:

- Recopilación de Datos: Recolectamos información personal, como nombre, dirección de correo electrónico y detalles de ejercicio, con el fin de proporcionar servicios personalizados y mejorar la experiencia del usuario.

- Uso de los Datos: Utilizamos los datos recopilados para ofrecer funcionalidades específicas de la aplicación, como la creación de rutinas de ejercicio personalizadas y el seguimiento de progresos. No compartimos información personal con terceros sin el consentimiento del usuario, excepto cuando sea requerido por ley.

- Seguridad de los Datos: Implementamos medidas de seguridad técnicas y organizativas para proteger los datos de los usuarios contra el acceso no autorizado, la divulgación o la alteración. Esto incluye el uso de en

criptación de datos y la limitación del acceso a la información personal.

Para obtener más detalles sobre cómo recopilamos, utilizamos y protegemos los datos de los usuarios, consulta nuestra Política de Privacidad completa en [enlace a la política de privacidad].

## Términos de Uso

Nuestros Términos de Uso establecen las reglas y pautas para el uso de nuestra aplicación. Al utilizar la aplicación, aceptas cumplir con estos términos, que incluyen:

- Uso Adecuado: No debes utilizar la aplicación de manera que infrinja las leyes aplicables o los derechos de terceros. Esto incluye la publicación de contenido ofensivo, difamatorio o ilegal.

- Responsabilidad del Usuario: Eres responsable de cualquier contenido que publiques o compartas a través de la aplicación. Asegúrate de tener los derechos necesarios para compartir dicho contenido y respeta los derechos de propiedad intelectual de terceros.

- Modificaciones de los Términos: Nos reservamos el derecho de actualizar o modificar los Términos de Uso en cualquier momento. Te notificaremos cualquier cambio significativo y deberás aceptar los nuevos términos para continuar utilizando la aplicación.

