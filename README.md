# ControlEscolarWeb

## Descripción

**ControlEscolarWeb** es una aplicación web desarrollada con HTML, CSS y JavaScript cuyo propósito es simular un sistema de gestión académica para instituciones educativas. El proyecto permite administrar alumnos, docentes, materias, grupos, calificaciones, asistencias y consultar información académica mediante una interfaz sencilla e intuitiva.

Además de sus funcionalidades básicas, el proyecto tiene como objetivo principal demostrar el uso de herramientas de control de versiones y trabajo colaborativo mediante Git y GitHub.

---

## Objetivos

* Simular un sistema de control escolar completo.
* Aplicar buenas prácticas de organización de proyectos web.
* Implementar un flujo de trabajo colaborativo utilizando Git y GitHub.
* Gestionar ramas, commits, pull requests y procesos de integración.
* Fortalecer las habilidades de desarrollo en equipo.
* Demostrar el consumo de APIs REST desde el frontend.

---

## Funcionalidades

### Módulo de Autenticación

* **Inicio de sesión seguro**: Autenticación de usuarios mediante JWT (JSON Web Tokens).
* **Encriptación de contraseñas**: Las contraseñas se almacenan de forma segura utilizando bcrypt.
* **Control de acceso por roles**: Cada usuario accede únicamente a su módulo correspondiente (admin, teacher, student).
* **Protección de rutas**: Las vistas están protegidas y solo accesibles con un token válido.
* **Cierre de sesión**: Eliminación del token para finalizar la sesión de forma segura.

### Módulo de Administración (Control Escolar)

* **RF-03 Gestión de Alumnos**: Dar de alta, baja, modificar y consultar información personal y académica de los alumnos (inscripciones, datos de contacto).
* **RF-04 Gestión de Docentes**: Registro, edición y asignación de profesores a sus respectivas materias y grupos.
* **RF-05 Gestión de Materias y Grupos**: Creación de asignaturas, planes de estudio, horarios y asignación de cupos por grupo (máximo 25 personas por grupo).

### Módulo de Docentes

* **RF-06 Registro de Calificaciones**: Los docentes pueden ingresar y modificar las notas de los alumnos inscritos en sus materias durante los periodos permitidos.
* **RF-07 Control de Asistencia**: Pasar lista y registrar asistencias/inasistencias de los estudiantes.

### Módulo de Alumnos

* **RF-08 Consulta de Historial Académico**: Visualizar calificaciones parciales, finales y promedio general (Kardex).
* **RF-09 Consulta de Horarios**: Mostrar materias inscritas, días, horas y docentes asignados.

---

## Tecnologías utilizadas

* HTML5
* CSS3
* JavaScript (ES6+)
* API (consumo de servicios REST)
* Git
* GitHub

---

## Estructura del proyecto

```
ControlEscolar
│
├── api
│   ├── config.js
│   └── client.js
│
├── services
│   ├── admin.service.js
│   ├── teacher.service.js
│   └── student.service.js
│
├── scripts
│   ├── admin.js
│   ├── teacher.js
│   ├── student.js
│   ├── login.js
│   └── index.js
│
├── styles
│   ├── admin.css
│   ├── teacher.css
│   ├── student.css
│   ├── login.css
│   └── index.css
│
├── views
│   ├── admin.html
│   ├── teacher.html
│   └── student.html
│
├── index.html
├── login.html
└── README.md
```

---

## Flujo de trabajo Git

El proyecto utiliza una estrategia basada en ramas para facilitar el desarrollo colaborativo.

### Ramas principales

- **main**: versión estable del proyecto.
- **develop**: rama de integración y pruebas.

### Ramas de funcionalidades

- **feature/admin**: Módulo de Administración (RF-03, RF-04, RF-05)
- **feature/teacher**: Módulo de Docentes (RF-06, RF-07)
- **feature/student**: Módulo de Alumnos (RF-08, RF-09)

Cada integrante desarrolla su funcionalidad en una rama independiente y posteriormente realiza un Pull Request para integrar los cambios a `develop`.

---

## Equipo de desarrollo

| Integrante | Responsabilidad |
|------------|------------------|
| Administrador | Configuración inicial, documentación, integración y gestión del repositorio |
| Desarrollador 1 | Módulo de Administración (feature/admin) |
| Desarrollador 2 | Módulo de Docentes (feature/teacher) |
| Desarrollador 3 | Módulo de Alumnos (feature/student) |

---

## Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/LuciaLeyva19/ControlEscolarWeb.git
