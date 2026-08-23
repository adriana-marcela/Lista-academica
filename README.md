# 📚Lista Académica

Aplicación web desarrollada con **Python** y **Django** para la gestión de cursos académicos. Permite registrar, editar, listar y eliminar cursos (código, nombre y número de créditos) desde una interfaz sencilla construida con Bootstrap.

## ✨ Funcionalidades

- **Registro de cursos**: alta de nuevos cursos con código, nombre y créditos.
- **Listado dinámico**: visualización en tabla de todos los cursos registrados.
- **Edición de cursos**: actualización de nombre y créditos de un curso existente.
- **Eliminación de cursos**: baja de cursos con confirmación previa (vía JavaScript).
- **Mensajes de confirmación**: feedback visual al usuario tras cada operación (registrar, actualizar, eliminar).
- **Panel de administración de Django** habilitado para gestión directa desde `/admin`.

## 🛠️ Tecnologías utilizadas 🐍

- **Backend**: Python, Django
- **Base de datos**: SQLite
- **Frontend**: HTML, CSS, JavaScript, Bootstrap 4
- **Otros**: jQuery, Popper.js

## 📁 Estructura del proyecto

```
Lista-academica/
├── academico/              # App principal (lógica de negocio)
│   ├── models.py           # Modelo Curso (código, nombre, créditos)
│   ├── views.py            # Vistas: home, registrar, editar, eliminar
│   ├── urls.py              # Rutas de la app
│   ├── static/              # CSS y JS
│   └── templates/           # Plantillas HTML (base, gestión y edición)
├── proyecto/                # Configuración del proyecto Django
│   ├── settings.py
│   └── urls.py
└── manage.py
```

## 🚀 Instalación y ejecución local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/Lista-academica.git
   cd Lista-academica
   ```

2. Crea y activa un entorno virtual:
   ```bash
   python -m venv venv
   source venv/bin/activate   # En Windows: venv\Scripts\activate
   ```

3. Instala las dependencias:
   ```bash
   pip install django
   ```

4. Aplica las migraciones de la base de datos:
   ```bash
   python manage.py migrate
   ```

5. (Opcional) Crea un superusuario para acceder al panel de administración:
   ```bash
   python manage.py createsuperuser
   ```

6. Levanta el servidor de desarrollo:
   ```bash
   python manage.py runserver
   ```

7. Abre tu navegador en `http://127.0.0.1:8000/`

## 📌 Modelo de datos

| Campo     | Tipo                     | Descripción                  |
|-----------|--------------------------|-------------------------------|
| `codigo`  | CharField (6, PK)        | Identificador único del curso |
| `nombre`  | CharField (50)           | Nombre del curso              |
| `creditos`| PositiveSmallIntegerField| Número de créditos del curso  |

## 🎯 Motivación

Este proyecto fue desarrollado como práctica de desarrollo web con Django, aplicando el patrón MVT (Model-View-Template) y operaciones CRUD completas sobre una entidad académica.

## 👩‍💻 Autora

Desarrollado por **Adriana Marcela** como parte de su portafolio de proyectos.

## 📄 Licencia

Este proyecto se distribuye con fines educativos y de portafolio.
