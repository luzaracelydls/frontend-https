# Protocolo HTTP 

El protocolo HTTP nos permite solicitar datos y recursos a un servidor. Estos pueden ser basados en una base de datos o contenido para un sitio web, ejemplo: un video o una base de datos.

## Flujo
Abre conexión
Hace petición
Lee respuesta 
Cierra conexión

## Métodos en una solicitud HTTP
GET
POST
PUT (UPDATE)
DELETE
Tú puedes describir en tu solicitud HTTP qué tipo de valor esperas, ejemplo JSON (en bases de datos) o mp4 para el caso de videos.

En Javascript, podemos implementar consultas a servidor a través de:
Uso de librerías como jQuery
APIs de Javascript:
AJAX / XMLHttpRequest (Es un estándar que tiene soporte de navegadores anteriores y actuales)
Fetch (esto es lo más nuevo y es basado en promesas, es decir, funciones asíncronas que realizan una operación y tienen un retorno de un valor resultante como completado o fallo)

## Estructura de una Solicitud
### Cabecera
Aporta información adicional

### Cuerpo
Mensaje. Generalmente este lo utilizamos en el método POST y PUT ya que enviamos información al servidor.

### Método
Campo obligatorio. Indica el tipo de solicitud 

### Path (Ruta)
La dirección del recurso a consultar

### Códigos de respuestas de Solicitudes

|  Codigo  | Tipo  | 
|---|---|
|  100 a 199 | Informativas  | 
|  200 a 299 | Exitosas  | 
|  300 a 399 | Redirecciones  |
|  400 a 499 | Errores  de clientes (acceso, conexion)  |
|  500 a 599 | Errores de servidor ("Internal Server Error", "Service Unavailable", "Timeout")  |



## Sintaxis
### AJAX (XMLHttPRequest)
`const xhr = new XMLHttpRequest();
xhr.open("GET", "https://jsonplaceholder.typicode.com/users");
xhr.send();
xhr.responseType = "json";
xhr.onload = () => {
  if (xhr.readyState == 4 && xhr.status == 200) {
    const data = xhr.response;
    console.log(data);
  } else {
    console.log('Error: ${xhr.status}');
  }
};`

### Promesas
`qwest.get('https://jsonplaceholder.typicode.com/posts')`
`.then((xhr, response) => console.log(response));`

# Referencias
1. https://kinsta.com/blog/javascript-http-request/?classId=31656c94-23a9-47be-b3ed-a16f5f1273a4&assignmentId=a723ebce-f1e7-4fce-8279-f5cf101a852d&classId=3ee93462-8ac4-4aa7-b01c-af8a6350f0d5&assignmentId=38b1d8d2-d664-4898-be15-0b986d5f2c14&classId=d320c43f-5113-41f9-9d3b-f42883b3ae87&assignmentId=a168c004-275d-4dd9-b77a-b622408e8b52
2. https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Status?classId=3ee93462-8ac4-4aa7-b01c-af8a6350f0d5&assignmentId=38b1d8d2-d664-4898-be15-0b986d5f2c14&classId=d320c43f-5113-41f9-9d3b-f42883b3ae87&assignmentId=a168c004-275d-4dd9-b77a-b622408e8b52
3. https://openweathermap.org/?classId=31656c94-23a9-47be-b3ed-a16f5f1273a4&classId=3ee93462-8ac4-4aa7-b01c-af8a6350f0d5&classId=d320c43f-5113-41f9-9d3b-f42883b3ae87&assignmentId=a723ebce-f1e7-4fce-8279-f5cf101a852d&assignmentId=38b1d8d2-d664-4898-be15-0b986d5f2c14&assignmentId=a168c004-275d-4dd9-b77a-b622408e8b52

