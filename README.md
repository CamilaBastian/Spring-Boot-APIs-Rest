# API REST – Gestión de Productos

API desarrollada como trabajo práctico integrador para la materia **Desarrollo De Software**, basada en arquitectura en capas, validaciones, manejo global de errores, persistencia con JPA/H2 y documentación con Swagger/OpenAPI.

## Descripción del Proyecto

Esta API REST permite gestionar productos de un e-commerce básico. Incluye creación, actualización, eliminación, consulta por ID y filtrado por categoría.
El proyecto implementa buenas prácticas profesionales:

* Arquitectura en capas (controller, service, repository, model, dto, exception)
* Validación de datos con **Bean Validation**
* Manejo centralizado de errores con **@ControllerAdvice**
* Persistencia con **Spring Data JPA + H2 Database**
* Documentación automática con **Swagger/OpenAPI**
* Uso de DTOs para desacoplar el modelo de dominio de las solicitudes/respuestas

---

## Tecnologías Utilizadas

* **Java 17+**
* **Spring Boot 3.x**
* **Spring Web**
* **Spring Data JPA**
* **H2 Database**
* **Bean Validation (Jakarta Validation)**
* **Lombok**
* **Spring Boot DevTools**
* **Swagger/OpenAPI (springdoc-openapi)**
* **Maven**

---

## Instrucciones para Clonar y Ejecutar el Proyecto

1. **Clonar el repositorio**

```bash
git clone https://github.com/tu-usuario/productos-api.git
cd productos-api
```

2. **Ejecutar la aplicación**

```bash
mvn spring-boot:run
```

3. **Acceder a la API**

* Swagger UI:
  [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)
* Consola H2:
  [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

  * JDBC URL (según configuración): `jdbc:h2:mem:productosdb`
  * Usuario: `sa`
  * Clave: *(vacía)*

---

## Endpoints de la API

| Método     | Ruta                                   | Descripción                                 |
| ---------- | -------------------------------------- | ------------------------------------------- |
| **GET**    | `/api/productos`                       | Lista todos los productos                   |
| **GET**    | `/api/productos/{id}`                  | Obtiene un producto por ID                  |
| **GET**    | `/api/productos/categoria/{categoria}` | Filtra productos por categoría              |
| **POST**   | `/api/productos`                       | Crea un nuevo producto (valida DTO)         |
| **PUT**    | `/api/productos/{id}`                  | Actualiza un producto completo              |
| **PATCH**  | `/api/productos/{id}/stock`            | Actualiza únicamente el stock               |
| **DELETE** | `/api/productos/{id}`                  | Elimina un producto por ID (204 No Content) |

---

## Accesos Útiles

* **Swagger UI:**
  [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)
* **Consola H2:**
  [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

---

## Capturas Obligatorias

![POST correcto](https://github.com/user-attachments/assets/f3b838e4-f757-43eb-9922-1a6b8ef2b1ca)
![H2](https://github.com/user-attachments/assets/1878172a-a567-4c5a-8208-243a6ee8188c)
![GET CORRECTO](https://github.com/user-attachments/assets/1e9a2fe7-1cba-47c2-8440-f00499d0dcaa)
![Error404 - GET](https://github.com/user-attachments/assets/c7c1f842-53b4-4265-9c60-9f83aa095d05)
![Error400 - GET](https://github.com/user-attachments/assets/53cb2759-8f17-488f-b6d0-615f2b225ced)


---

## Autor

**Nombre:** Camila Bastian
**Legajo:** 50795

---

