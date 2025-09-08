# Servidor JSON Simulado para Sistema de Mesa de Ayuda

Este repositorio contiene un servidor JSON simulado en typicode solo puede simular GET.

## Estructura de datos

### Usuarios

- GET `/usuarios?id=XXX` - Obtener usuario por ID
- POST `/usuarios/registrar` - Registrar nuevo usuario (NO se puede simular solo se permite GET)
- POST `/usuarios/login` - Login de usuario (NO se puede simular solo se permite GET)
- POST `/usuarios/logout` - Logout de usuario (NO se puede simular solo se permite GET)

### Tickets
- GET `/tickets?id=XXX` - Obtener ticket por ID
- POST `/ticket/crear` - Crear nuevo ticket (NO se puede simular solo se permite GET)
- PUT `/actualizar/ticket?id=XXX` - Actualizar ticket (NO se puede simular solo se permite GET)

## Server emulator como Typicode

Accede a los endpoints en:
`https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/`

### Ejemplos:
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios?id=803a62c8-78c8-4b63-9106-73af215d504b
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets?id=12345

## Nota:
- Para operaciones completas de escritura, se necesita implementar un servidor JSON Server local
