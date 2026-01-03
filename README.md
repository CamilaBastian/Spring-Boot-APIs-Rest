# 🛒 API REST - Gestión de Productos

![Java](https://img.shields.io/badge/Java-17%2B-orange?style=flat-square&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green?style=flat-square&logo=springboot)
![Swagger](https://img.shields.io/badge/Swagger-OpenAPI-85EA2D?style=flat-square&logo=swagger)
![H2](https://img.shields.io/badge/Database-H2-blue?style=flat-square)

> **Trabajo Práctico**
> Asignatura: *Desarrollo de Software*

---

## 📄 Descripción del Proyecto

Esta API REST permite la gestión integral de productos para un sistema de e-commerce. El objetivo principal es demostrar la implementación de una **arquitectura de software profesional** utilizando Spring Boot, asegurando la integridad de datos y un manejo robusto de errores.

El proyecto se construyó siguiendo buenas prácticas de ingeniería de software, desacoplando la lógica de negocio de la capa de presentación y persistencia.

## 🏗 Arquitectura y Diseño

El sistema implementa una **Arquitectura en Capas** estricta:

1.  **Controller Layer:** Manejo de peticiones HTTP.
2.  **Service Layer:** Lógica de negocio.
3.  **Repository Layer:** Acceso a datos (JPA).
4.  **Model/Domain:** Entidades del sistema.
5.  **DTOs:** Transferencia de datos segura.
6.  **Exception Handling:** `@ControllerAdvice` para respuestas de error uniformes.

### Características Clave
* ✅ **Validaciones:** Uso de *Bean Validation* (Jakarta) para asegurar la integridad de los datos de entrada.
* ✅ **Manejo de Errores:** Respuestas JSON estandarizadas para errores 400, 404, etc.
* ✅ **Persistencia:** Base de datos H2 en memoria para desarrollo rápido.
* ✅ **Documentación:** Swagger UI integrado para pruebas interactivas.

---

## 🛠 Stack Tecnológico

* **Core:** Java 17+, Spring Boot 3.x
* **Web:** Spring Web (REST)
* **Datos:** Spring Data JPA, H2 Database
* **Utilidades:** Lombok, Spring Boot DevTools
* **Validación:** Jakarta Validation API
* **Docs:** SpringDoc OpenAPI (Swagger)
* **Build:** Maven

---

## 📡 Endpoints de la API

Documentación interactiva disponible en: `http://localhost:8080/swagger-ui/index.html`

| Método | Ruta | Descripción |
| :--- | :--- | :--- |
| `GET` | `/api/productos` | Lista todos los productos disponibles. |
| `GET` | `/api/productos/{id}` | Obtiene el detalle de un producto específico. |
| `GET` | `/api/productos/categoria/{cat}`| Filtra productos por su categoría. |
| `POST` | `/api/productos` | Crea un nuevo producto (requiere Body JSON). |
| `PUT` | `/api/productos/{id}` | Actualiza totalmente un producto existente. |
| `PATCH`| `/api/productos/{id}/stock` | Actualiza únicamente el stock (operación ligera). |
| `DELETE`| `/api/productos/{id}` | Elimina un producto (Soft delete o físico según config). |

---

## 📸 Galería de Funcionamiento

### ✅ Casos Exitosos

**1. Creación de Producto (POST)**
![POST correcto](https://github.com/user-attachments/assets/f3b838e4-f757-43eb-9922-1a6b8ef2b1ca)

**2. Consulta Exitosa (GET)**
![GET CORRECTO](https://github.com/user-attachments/assets/1e9a2fe7-1cba-47c2-8440-f00499d0dcaa)

**3. Persistencia en Base de Datos (H2 Console)**
![H2](https://github.com/user-attachments/assets/1878172a-a567-4c5a-8208-243a6ee8188c)

### ❌ Manejo de Errores

**1. Recurso No Encontrado (404 Not Found)**
![Error404 - GET](https://github.com/user-attachments/assets/c7c1f842-53b4-4265-9c60-9f83aa095d05)

**2. Error de Validación (400 Bad Request)**
![Error400 - GET](https://github.com/user-attachments/assets/53cb2759-8f17-488f-b6d0-615f2b225ced)

---

## 🚀 Instrucciones de Ejecución

1.  **Clonar el repositorio:**
    ```bash
    git clone https://github.com/CamilaBastian/Spring-Boot-APIs-Rest.git
    cd productos-api
    ```

2.  **Ejecutar la aplicación:**
    ```bash
    mvn spring-boot:run
    ```

3.  **Verificar funcionamiento:**
    * Swagger UI: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)
    * H2 Console: [http://localhost:8080/h2-console](http://localhost:8080/h2-console)
        * *JDBC URL:* `jdbc:h2:mem:productosdb`
        * *User:* `sa`
        * *Pass:* (vacío)

---

## 👤 Autor

**Camila Bastian**
*Desarrollo de Software*

