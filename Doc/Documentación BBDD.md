

## Base de Datos

FitZone utiliza una base de datos relacional para almacenar y gestionar la información de los usuarios, rutinas de ejercicio, progresos y publicaciones sociales. A continuación, se detallan las tablas principales y sus campos:

### Tabla: users

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| name       | varchar(255) | Not null         |
| email      | varchar(255) | Not null, Unique |
| password   | varchar(255) | Not null         |
| height     | decimal(5,2) |                  |
| weight     | decimal(5,2) |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

### Tabla: routines

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| user_id    | int          | Foreign Key      |
| name       | varchar(255) | Not null         |
| description| text         |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

### Tabla: exercises

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| routine_id | int          | Foreign Key      |
| name       | varchar(255) | Not null         |
| sets       | int          |                  |
| reps       | int          |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

### Tabla: progress

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| user_id    | int          | Foreign Key      |
| exercise_id| int          | Foreign Key      |
| weight     | decimal(5,2) |                  |
| reps       | int          |                  |
| date       | date         |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

### Tabla: posts

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| user_id    | int          | Foreign Key      |
| content    | text         |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

### Tabla: available_exercises

| Campo      | Tipo         | Restricciones    |
|------------|--------------|------------------|
| id         | int          | Primary Key      |
| name       | varchar(255) | Not null         |
| description| text         |                  |
| created_at | timestamp    |                  |
| updated_at | timestamp    |                  |

---

Aquí tienes un ejemplo de cómo podría lucir la base de datos completa con datos por defecto:

### Tabla: users

| id | name     | email              | password    | height | weight | created_at          | updated_at          |
|----|----------|--------------------|-------------|--------|--------|---------------------|---------------------|
| 1  | John Doe | johndoe@example.com| hashedpass1 | 175.50 | 80.00  | 2023-06-01 09:12:45 | 2023-06-01 09:12:45 |
| 2  | Jane Doe | janedoe@example.com| hashedpass2 | 165.25 | 65.75  | 2023-06-02 14:30:18 | 2023-06-02 14:30:18 |

### Tabla: routines

| id | user_id | name             | description                         | created_at          | updated_at          |
|----|---------|------------------|-------------------------------------|---------------------|---------------------|
| 1  | 1       | Full Body Workout| Workout targeting all major muscle groups. | 2023-06-03 10:45:12 | 2023-06-03 10:45:12 |
| 2  | 1       | Cardio HIIT      | High-intensity interval training for cardiovascular health. | 2023-06-05 16:20:05 | 2023-06-05 16:20:05 |
| 3  | 2       | Upper Body Push  | Upper body strength training exercises.  | 2023-06-04 12:15:30 | 2023-06-04 12:15:30 |

### Tabla: exercises

| id | routine_id | name          | sets | reps | created_at          | updated_at          |
|----|------------|---------------|------|------|---------------------|---------------------|
| 1  | 1          | Squats        | 3    | 10   | 2023-06-03 10:46:25 | 2023-06-03 10:46:25 |
| 2  | 1          | Bench Press   | 3    | 8    | 2023-06-03 10:47:41 | 2023-06-03 10:47:41 |
| 3  | 2          | Jumping Jacks | 1    | 20   | 2023-06-05 16:21:55 | 2023-06-05 16:21:55 |
| 4  | 2          | Burpees       | 1    | 12   | 2023-06-05 16:23:10 | 2023-06-05 16:23:10 |
| 5  | 3          | Push-ups      | 3    | 12   | 2023-06-04 12:16:45 | 2023-06-04 12:16:45 |
| 6  | 3          | Shoulder Press| 3    | 10   | 2023-06-04 12:18:02 | 2023-06-04 12:18:02 |

### Tabla: progress

| id | user_id | exercise_id | weight | reps | date       | created_at          | updated_at          |
|----|---------|-------------|--------|------|------------|---------------------|---------------------|
| 1  | 1       | 1           | 100.00 | 10   | 2023-06-03 | 2023-06-03 10:47:52 | 2023-06-03 10:47:52 |
| 2  | 1       | 2           | 80.00  | 8    | 2023-06-03 | 2023-06-03 10:48:15 | 2023-06-03 10:48:15 |
| 3  | 2       | 3           | 0.00   | 20   | 2023-06-05 | 2023-06-05 16:23:35 | 2023-06-05 16:23:35 |
| 4  | 2       | 4           | 0.00   | 12   | 2023-06-05 | 2023-06-05 16:23:58 | 2023-06-05 16:23:58 |
| 5  | 1       | 1           | 110.00 | 12   | 2023-06-06 | 2023-06-06 09:35:21 | 2023-06-06 09:35:21 |

### Tabla: posts

| id | user_id | content                                      | created_at          | updated_at          |
|----|---------|----------------------------------------------|---------------------|---------------------|
| 1  | 1       | Working hard at the gym! #FitZone #Fitness    | 2023-06-04 18:30:40 | 2023-06-04 18:30:40 |
| 2  | 2       | Feeling great after today's workout! 💪       | 2023-06-05 09:15:10 | 2023-06-05 09:15:10 |



| id | name            | description                                       | created_at          | updated_at          |
|----|-----------------|---------------------------------------------------|---------------------|---------------------|
| 1  | Squats          | Compound exercise targeting the lower body muscles| 2023-06-01 09:12:45 | 2023-06-01 09:12:45 |
| 2  | Bench Press     | Compound exercise targeting the chest muscles     | 2023-06-01 09:12:45 | 2023-06-01 09:12:45 |
| 3  | Lunges          | Exercise targeting the leg muscles                | 2023-06-01 09:12:45 | 2023-06-01 09:12:45 |


Este ejemplo muestra datos ficticios para las tablas principales de la base de datos. 

---

La base de datos para la aplicación FitZone se ha diseñado para permitir el seguimiento de rutinas de ejercicio, el registro de progreso individual y la interacción social entre los usuarios. Aquí tienes una descripción del funcionamiento de esta base de datos:

1. La tabla `users` almacena la información de los usuarios registrados, como su nombre, correo electrónico, contraseña, altura y peso. Los usuarios pueden registrar su información personal y utilizarla para un seguimiento preciso de su progreso físico.

2. La tabla `routines` guarda las rutinas de ejercicio creadas por los usuarios. Cada rutina tiene un nombre y una descripción. Los usuarios pueden crear y personalizar sus propias rutinas o seleccionar rutinas predefinidas.

3. La tabla `exercises` almacena los ejercicios individuales asociados a cada rutina. Cada ejercicio tiene un nombre, número de series y número de repeticiones. Los usuarios pueden agregar ejercicios a sus rutinas y personalizar los parámetros de cada ejercicio según sus necesidades.

4. La tabla `progress` permite hacer un seguimiento del progreso de los usuarios en los ejercicios. Registra el peso utilizado, el número de repeticiones y la fecha en que se realizó cada ejercicio. Esto permite a los usuarios monitorear su evolución a lo largo del tiempo y ajustar sus rutinas según sea necesario.

5. La tabla `posts` guarda las publicaciones realizadas por los usuarios en la zona social de la aplicación. Cada publicación tiene un contenido de texto que describe la publicación. Los usuarios pueden compartir su progreso, fotos o cualquier otra información relevante relacionada con su experiencia en el gimnasio.

Además, se ha agregado la tabla `available_exercises` que almacena una lista de todos los ejercicios disponibles. Esto permite cargar ejercicios predefinidos en las rutinas de los usuarios y facilita la selección de ejercicios al crear nuevas rutinas.

En resumen, esta base de datos brinda la funcionalidad necesaria para que los usuarios registren su información personal, creen y gestionen sus rutinas de ejercicio, realicen un seguimiento de su progreso y compartan su experiencia a través de publicaciones en la zona social. Todo esto con el objetivo de ayudar a los usuarios a alcanzar sus objetivos de acondicionamiento físico y mantenerse motivados en su viaje hacia una vida saludable.
