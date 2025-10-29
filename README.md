# Taller: Sistema de Gestión de Estudiantes y Cursos

## Objetivo general
Desarrollar una API REST completa aplicando arquitectura por capas (**API**, **Application**, **Domain**, **Infrastructure**), **Entity Framework Core** y **MySQL**, que permita administrar estudiantes, cursos e inscripciones.

El objetivo es que el estudiante demuestre dominio de:

- La estructura de una solución limpia.  
- El uso de **EF Core** con migraciones.  
- La **inyección de dependencias**.  
- El consumo de **endpoints desde Postman**.  
- Las **relaciones entre entidades**.

---

## Contexto del problema
Una institución educativa necesita un sistema que permita gestionar la información de sus **estudiantes**, **cursos** y las **inscripciones** que relacionan a ambos.

El sistema debe permitir registrar estudiantes, crear cursos y asignar estudiantes a los cursos.  
Además, los usuarios deben poder consultar qué estudiantes están inscritos en un curso específico y qué cursos tiene asignado un estudiante.

---

## Requerimientos técnicos

1. Crear una solución vacía y dentro de ella los siguientes proyectos:
   - `webEscuela.Api`
   - `webEscuela.Application`
   - `webEscuela.Domain`
   - `webEscuela.Infrastructure`

2. Configurar las referencias entre proyectos de forma correcta, manteniendo el principio de **independencia del dominio**.

3. Usar **MySQL** con **Entity Framework Core** y **migraciones**.

4. Organizar el código respetando la responsabilidad de cada capa:
   - **Domain:** Entidades e interfaces.  
   - **Infrastructure:** Contexto de base de datos y repositorios.  
   - **Application:** Servicios con la lógica de negocio.  
   - **API:** Controladores, inyección de dependencias y endpoints.

---

## Requerimientos funcionales

### Estudiantes
- Registrar un nuevo estudiante.  
- Listar todos los estudiantes.  
- Obtener un estudiante por su ID.  
- Actualizar la información de un estudiante.  
- Eliminar un estudiante.

### Cursos
- Crear un nuevo curso.  
- Listar todos los cursos.  
- Obtener un curso por su ID.  
- Actualizar la información de un curso.  
- Eliminar un curso.

### Inscripciones
- Registrar una inscripción (asignar un estudiante a un curso).  
- Listar todas las inscripciones.  
- Consultar los cursos en los que está inscrito un estudiante.  
- Consultar los estudiantes inscritos en un curso específico.

---

## Relaciones
- Un **estudiante** puede estar inscrito en varios cursos.  
- Un **curso** puede tener varios estudiantes inscritos.  
- La relación debe gestionarse mediante una **tabla intermedia** (por ejemplo, `Inscripciones`).
