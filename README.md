# TablaApiJAGC

El proyecto fue realizado con angular [Angular CLI](https://github.com/angular/angular-cli) version 18.2.11.

## Explicación de la práctica 

## Creación del proyecto
Como primer paso debemos crear un nuevo proyecto en angular para eso utilizamos el comando:  `ng new tabla-api-JAGC`. Despues crearemos un componente llamado users como se solicita en la instrucciones de la práctica `ng generate component users`.

![image](https://github.com/user-attachments/assets/379e9a00-2027-45df-b4b2-e79495a108b3)

## Creación del servicio para consumir una api

Crearemos la carpeta services donde solo crearemos un archivo nuevo nombrado `user.service.ts`.
apiUrl: Es una variable privada que almacena la URL base de la API que vamos a consumir.
constructor(private http: HttpClient): Inyecta el servicio HttpClient de Angular, que se utilizará para hacer las solicitudes HTTP.

● Pregunta: ¿Qué hace el método getUsers en este servicio?

El método getUsers() recupera una lista de usuarios desde la API especificada o en este caso la que consigue de apiUrl.

![image](https://github.com/user-attachments/assets/2fe2d3bd-76cd-487b-a062-38e4d72d7ca2)


## Crear el Componente de la Tabla de Usuarios

Genera un componente llamado users en el cual la intención es crear el molde de la tabla y ademas poder colocar los metodos que se encargan del funcionamiento de la tabla y acomodar los datos

● ¿Qué función cumple el método ngOnInit en el componente UserListComponent?
Cumple con la función de llamar al método loadUsers cuando el componente se inicializa ademas el loadUsers se encarga de iniciar la carga de los datos de usuarios desde la API y actualizar el estado del componente.Esto sirve es para cualquier inicialización que necesite acceso a las propiedades del componente, como cargar datos desde una API

![image](https://github.com/user-attachments/assets/5ef21012-915b-4e07-bb45-d79a6f5a6f11)


## Crear el Componente de la Tabla de Usuarios

La tabla se creo desde el mismo .ts ya que utilizando las comillas siguientes "``" podemos hacer refrencias al formato que queremos sin la necesidad de poner otro html o un css.

● ¿Para qué sirve el bucle *ngFor en Angular?
Se utiliza para repetir un elemento HTML para cada elemento de una colección. Básicamente, permite iterar sobre una lista de datos obtiene una lista de usuarios desde la API y la almacena en la propiedad users.

![image](https://github.com/user-attachments/assets/c4c0ff03-dc71-4e89-841e-66f443a5b43b)


## Ejecutar el Proyecto

Finalmente se ejecuta el proyecto con el siguiente comando: `ng serve -o` para abrir en automatico:

![image](https://github.com/user-attachments/assets/11139f87-be17-4f64-8fd2-34f9b641ba7e)

## Preguntas de reflexión final:

1. ¿Qué ventajas tiene el uso de servicios en Angular para el consumo de APIs?
Reutilización del código para manejar peticiones a APIs.
Centralización de la lógica de consumo, facilitando el mantenimiento.
Separación de responsabilidades, manteniendo los componentes limpios.
2. ¿Por qué es importante separar la lógica de negocio de la lógica de presentación?
Esta separación nos permite reutilizar la lógica de negocio en diferentes partes de la aplicación o incluso en otros proyectos, y facilita hacer cambios en la interfaz sin afectar la funcionalidad principal.
3. ¿Qué otros tipos de datos o APIs podrías integrar en un proyecto como este?
Algunas APIs para autenticación (OAuth, Firebase Auth) o para recuperación de contraseñas, o incluso APIs de mapas como Google Maps para ubicaciones. Esto enriquece la funcionalidad de este proyecto y nos permite combinar servicios externos con nuestra lógica.
