# UrbanFlow Backend (PostgreSQL + Roles)

Backend en Node.js con Express y PostgreSQL con gestión de usuarios y roles.

## Instalación
```bash
npm install
npm start
```

## Endpoints principales añadidos

- `POST /api/users/register` - Registrar usuario. Body: `{ name, email, password, roles? }`
- `POST /api/users/login` - Login. Body: `{ email, password }`
- `GET /api/users/` - Listar usuarios (no paginado).
- `GET /api/users/:id` - Obtener usuario por id.
- `PUT /api/users/:id` - Actualizar usuario.
- `DELETE /api/users/:id` - Eliminar usuario.
- `POST /api/users/:id/roles` - Asignar roles a usuario. Body: `{ roles: [1,2] }`
- `DELETE /api/users/:id/roles/:roleId` - Quitar rol a usuario.

- `POST /api/roles/create` - Crear rol. Body: `{ name, description }`
- `GET /api/roles/` - Listar roles.
- `GET /api/roles/:id` - Obtener rol.
- `PUT /api/roles/:id` - Actualizar rol.
- `DELETE /api/roles/:id` - Eliminar rol.

Nota: se agregó un helper JWT en `utils/jwtHelper.js` (stub). No se implementó la gestión de cookies/almacenamiento de tokens

