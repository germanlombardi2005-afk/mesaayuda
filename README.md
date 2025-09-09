# Servidor JSON Simulado para Sistema de Mesa de Ayuda

Este repositorio contiene un servidor JSON simulado en typicode solo puede simular GET.

## Estructura de datos

### Usuarios

- GET `/usuarios?id=XXX` - Obtener usuario por ID
- POST `/usuarios/registrar` - Registrar nuevo usuario 
- POST `/usuarios/login` - Login de usuario 
- POST `/usuarios/logout` - Logout de usuario 

### Tickets
- GET `tickets` - Obtener todos los tickets
- GET `/tickets?id=XXX` - Obtener ticket por ID
- POST `/tickets` - Crear nuevo ticket
- PATCH `/tickets/XXX` - Actualizar ticket 

## Server emulator como Typicode

Accede a los endpoints en:
`https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/`

### Ejemplos:
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios?id=803a62c8-78c8-4b63-9106-73af215d504b
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets?id=12345

## Nota:
- AQUI SE PONGRAN EJEMPLOS PARA QUE SE PUEDA MODIFICAR RAPIDO Y FACIL. QUE SEA COPIAR Y PEGAR.
- TODO LO MENCIONADO SE DEBE HACER EN POSTMAN O EN LA APP DE TU PREFERENCIA. GOOGLE SOLO ADMITE GET
- COMENZEMOS CON PATCH MAS EN ESPECIFICO CAMBIAR LA DESCRIPCION DE UN TICKET
MODIFICAMOS EL TICKET: 12345
LINK PATCH: https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets/12345
En Headers: Key: Content-Type y Value: application/json
En Raw: JSON y cambiamos solo la descripcion:
{
  "descripcion": "Problemas para hacer una compra"
}

- AHORA SERA CREAR UN TICKET:
LINK "POST" https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets
Headers: Content-Type: application/json
En Raw (LA SIMULACION SOLO TE GENERA LA ID ESTO SE PUEDE CAMBIAR DESDE POSTMAN (usando Pre-request Script para te pida menos datos por ejemplo solo la descripcion y tu usuario id. Y el ponga la fecha y los estados "No verifique como funciona esto") O COMO YA DIMOS PODRIAS CREAR UN BACKEND PROPIO CON NODE.JS + EXPRESS):

{__
  "usuario_id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",__
  "descripcion": "No puedo acceder a mi cuenta",__
  "estado": "inicial",__
  "fecha_alta": "16/9/2025 15:30:00",__
  "fecha_cierre": null
}__

- ES MAS COMPLICADO SIMULAR UN LOGIN / REGISTER / LOGOUT SIN LOGICA PERO PODRIA SIMULARSE.
PODRIAS TAL VEZ HACER UN POST EN https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios FINGIENDO QUE PONES LA CONTRASEÑA Y EL CORREO:
{
  "contacto": "colla.pedro@gmail.com",
  "password": "secret"
}
Y LUEGO HACER UN: 
GET https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios?contacto=colla.pedro@gmail.com&password=secret