# 🐶 Backend III - Entrega Final

## Descripción

Este proyecto fue desarrollado como **Entrega Final del curso Backend III de Coderhouse**.

La aplicación consiste en una **API REST** desarrollada con **Node.js**, **Express** y **MongoDB**, destinada a gestionar usuarios, mascotas y procesos de adopción.

Como parte de la entrega se implementaron **tests funcionales**, la **dockerización completa del proyecto**, la **publicación de la imagen en Docker Hub** y la documentación necesaria para reproducir la aplicación.

---

# Tecnologías utilizadas

- Node.js
- Express
- MongoDB
- Mongoose
- Docker
- Docker Hub
- Mocha
- Chai
- Supertest
- Cookie Parser
- Dotenv

---

# Arquitectura del proyecto

El proyecto fue desarrollado utilizando una arquitectura por capas, separando las responsabilidades de cada componente para facilitar el mantenimiento, la escalabilidad y las pruebas.

La aplicación implementa los siguientes componentes:

- Controllers
- Routes
- Repository
- DAO (Data Access Object)
- DTO (Data Transfer Object)
- Services
- Utils

Además, se implementa el patrón **Repository**, desacoplando la lógica de negocio del acceso a los datos.

---

# Estructura del proyecto

```text
backend3-final
│
├── src
│   ├── controllers
│   ├── dao
│   │   └── models
│   ├── dto
│   ├── repository
│   ├── routes
│   ├── services
│   ├── utils
│   ├── public
│   └── app.js
│
├── tests
├── Dockerfile
├── .dockerignore
├── package.json
└── README.md
```

---

# Funcionalidades principales

La API permite:

- Registro de usuarios.
- Inicio de sesión.
- Administración de mascotas.
- Gestión de adopciones.
- Consulta de usuarios.
- Consulta de mascotas.
- Consulta de adopciones.

---

# Endpoints principales

## Usuarios

```
/api/users
```

## Mascotas

```
/api/pets
```

## Adopciones

```
/api/adoptions
```

## Sesiones

```
/api/sessions
```

---

# Instalación del proyecto

## 1. Clonar el repositorio

```bash
git clone https://github.com/Mati-Azar/backend3-final.git
```

## 2. Ingresar al proyecto

```bash
cd backend3-final
```

## 3. Instalar dependencias

```bash
npm install
```

## 4. Crear el archivo .env

Ejemplo:

```env
PORT=8080
MONGO_URI=tu_uri_de_mongodb
```

---

# Ejecución local

Iniciar la aplicación:

```bash
npm start
```

La API quedará disponible en:

```
http://localhost:8080
```

---

# Docker

## Construcción de la imagen

```bash
docker build -t backend3-final .
```

## Etiquetado

```bash
docker tag backend3-final pelambre/backend3-final:latest
```

## Ejecución del contenedor

```bash
docker run -p 8080:8080 --env-file .env pelambre/backend3-final:latest
```

---

# Tests funcionales

Los tests fueron desarrollados utilizando:

- Mocha
- Chai
- Supertest

Para ejecutarlos:

```bash
npm test
```

Los tests verifican:

- Registro de usuarios.
- Inicio de sesión.
- Creación de mascotas.
- Creación de adopciones.
- Consulta de adopciones.
- Manejo de errores y validaciones.

---

# Docker Hub

Imagen pública disponible en:

https://hub.docker.com/r/pelambre/backend3-final

---

# Repositorio GitHub

https://github.com/Mati-Azar/backend3-final

---

# Evidencias

Durante el desarrollo del proyecto se verificó correctamente:

- Construcción de la imagen Docker.
- Publicación de la imagen en Docker Hub.
- Escaneo básico de seguridad mediante Docker Scout.
- Ejecución satisfactoria del contenedor.
- Ejecución exitosa de los tests funcionales.

---

# Autor

**Matías Azar**

Entrega Final – Backend III

Coderhouse
