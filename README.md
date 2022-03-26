# Ensayo para la Demo

- Previamente se debe haber preparado la base de datos de prueba, mediante el archivo `seed.rb` (No utilizar el email _"email@email.com"_).
- Se debe conocer de antemano los parámetros del usuario con rol `admin`.

---
## Postman

### Auth

#### /auth/register
```sh
{"user": {
    "email":"email@email.com",
    "password":"password",
    "last_name":"last_name",
    "first_name":"first_name",
    }
}
```

> Mencionar token y que se crea como usuario rol 'XYZ'

---
#### /auth/login
```sh
{
    "email":"admin@email.com",
    "password":"admin_pass"
}
```
> Explicar que el user con rol admin, lo crean los administradores de la API

---
## Swagger

### Announcement

#### POST announcements
```sh
{
  "announcement": {
    "name": "Ultimo momento",
    "content": "El grupo 151 - Go Ruby, es lo máximo!!!!!!!!",
    "image": "/test.png",
    "category_id": <same_category>
  }
}
```

#### GET announcements/:id
- Cargar el `:id` del nuevo `announcement` 
- Cargar un `:id` invalido (`0`, `-1`, etc.)

#### PUT announcements/:id

- Ejemplo, de actualización invalida.
```sh
{
  "announcement": {
    "name": 1,
    "content": "*",
  }
}
```


- Ejemplo, de actualización valida.
```sh
{
  "announcement": {
    "name": "Ultimo momento!!!",
    "content": "El talentoso grupo 151 - Go Ruby, es lo máximo!!!!!",
  }
}
```

---
### Slide

#### GET slides
- Mostrar resultados no paginados.

---
### Testimonial

#### GET testimonials?page={page}

- Mostrar resultados paginados segun el valor de `page`.

