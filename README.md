# Servidor JSON Simulado para Sistema de Mesa de Ayuda

Este repositorio contiene un servidor JSON simulado para pruebas del sistema de mesa de ayuda.

## Estructura de datos

### Usuarios
- GET `/usuarios?id=XXX` - Obtener usuario por ID
- POST `/usuarios/registrar` - Registrar nuevo usuario (simulado)
- POST `/usuarios/login` - Login de usuario (simulado)
- POST `/usuarios/logout` - Logout de usuario (simulado)

### Tickets
- GET `/tickets?id=XXX` - Obtener ticket por ID
- POST `/ticket/crear` - Crear nuevo ticket (simulado)
- PUT `/actualizar/ticket?id=XXX` - Actualizar ticket (simulado)

## Uso con JSONPlaceholder

Accede a los endpoints en:
`https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/`

### Ejemplos:
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/usuarios?id=803a62c8-78c8-4b63-9106-73af215d504b
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets
- https://my-json-server.typicode.com/germanlombardi2005-afk/mesaayuda/tickets?id=12345

## Notas importantes
- JSONPlaceholder es de solo lectura, las operaciones POST/PUT son simuladas
- Para operaciones completas de escritura, se necesita implementar un servidor JSON Server local
