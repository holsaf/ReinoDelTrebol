# ReinoDelTrebolAPI

El API ReinoDelTrebol es un sistema que permite el registro, edicion, consulta y eliminacion de solicitudes de estudiantes de la academia de magia Reino del Trebol. Durante el registro se hace una asignacion aleatoria del Grimorio y una validacion de datos para su aprobacion o rechazo. Fue construida con el freamwork ASP.NET Core 6 y usa como motor de base de datos MySQL.

# Funciones de Soporte

  * El usuario puede enviar un solicitud de ingreso.
  * El usuario puede actualizar una solicitud de ingreso.
  * EL usuario puede actualizar el estado de un solicitud.
  * El usuario puede consultar todas las solicitudes registradas en la base de datos (aprobadas y rechazadas).
  * El usuario puede consultar la asignacion de Grimario de la solicitud de ingreso.
  * EL usuario puede eliminar una solicitud de ingreso.

# Pre-requisitos 

  * .NET Core 6
  
  * Local instance MySQL

# Guia de Instalacion
  * Clone el repositorio 
  
     ```
     git clone https://github.com/holsaf/ReinoDelTrebol.git.
     ```
     
  * Configure la conexion de la base de datos.
  
  1. Configure los datos de conexion en los "secretos de usuario" dando click derecho en ReinoTrebolApi.csproj.
  
  ![image](https://user-images.githubusercontent.com/87883786/201547680-3c9696aa-a14b-401b-b583-b9658eb20a3f.png)
  
  2. Reemplace la informacion de user (id,password) por los datos de su conexion local de MySQL.
  
  ![image](https://user-images.githubusercontent.com/87883786/201547707-f21da5f3-8331-4bc3-a46e-0f894b270e19.png)
  
  3. Ir a appsettings.json y configurar la conexion.
  
  ![image](https://user-images.githubusercontent.com/87883786/201547801-29c6f14c-f86f-4fd4-a6f3-bd840ec688a9.png)
  
  * Run 
  
    ```
    dotnet build 
    ```
    
  o click derecho en ReinoTrebolApi.csproj, para compilar el proyecto.

![image](https://user-images.githubusercontent.com/87883786/201547917-c8798410-6e62-4138-9f61-6ef2a1d9f3f9.png)

  * La migracion creara de forma automatica la base de datos en la primera compilacion del proyecto.

# Uso
  * Run 
  
    ```
    dotnet run --project ReinoTrebolApi/ReinoTrebolApi.csproj
    ```
    
  o dando click en la siguiente opcion del Visual Studio:

![image](https://user-images.githubusercontent.com/87883786/201548512-216dc50c-ed82-4016-8863-2c920e4788c0.png)

  * Conectese a la API usando POSTMAN en el puerto 
  
    ```
    https://localhost:7294.
    ```

# API Endpoints

| HTTP Verbs | Endpoints | Action |
| --- | --- | --- |
| POST | /api/solicitud | Eegistar una solicitud |
| PUT | /api/solicitud  | Actualizar una solicitud |
| GET | /api/solicitud | Consultar todas las solictudes |
| GET | /api/solicitud/grimorio/:Id | Consultar el grimorio asignado a una solicitud |
| PATCH | /api/solicitud/:Id | Actualizar el estado de una solicitud |
| DELETE | /api/solicitud/:Id | Eliminar una solicitud |

# Swagger

  * La documentacion de los endpoints se genera de forma automatica en la url:
  
  ```
   https://localhost:7294/swagger/index.html
  ```  

# Autores 
  
  Holman Sanchez Fuentes



