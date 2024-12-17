# <strong>pescaito-hub</strong>

Grupo 1

Curso escolar: 2024/2025

Asignatura: Evolución y gestión de la configuración

## Miembros del equipo: escala de 1 al 10 con el esfuerzo hecho en el proyecto (10 mayor implicación, 1 menor implicación)


Miembro	| Implicación:

| Apellidos, Nombre | [1-10] |
|-------------------|--------|
| Pizarro López, Eduardo | [8] |
| Garate Fuentes, Yesica | [7] |
| Portillo Sánchez, Alonso | [10] |
| Sevillano Barea, Alejandro | [10] |
| Espinosa Naranjo, Pablo | [10] |
| Harana Mancilla, Rafael | [5] |


## Enlaces de interés:
repositorio de código: https://github.com/pescaito-team/pescaito-hub
sistema desplegado:

| Miembro del equipo | Horas | Commits | LoC  | Test | Issues | Work Item          |
|--------------------|-------|---------|------|------|--------|--------------------|
| Pizarro López, Eduardo | HH    | XX      | YY   | ZZ   | II     | Permitir al usuario recibir una contraseña si tiene la configuración necesaria y restablecer su contraseña y cambiar su contraseña una vez iniciada la sesion. Se intento implementar el WI search querys el cual se avanzo hasta el punto de poder buscar por cadenas exactas en el buscador de datasets  |
| Garate Fuentes, Yesica | HH    | XX      | YY   | ZZ   | II     |  Permitir al usuario recibir una contraseña si tiene la configuración necesaria y restablecer su contraseña. Se intento implementar el WI search querys el cual se avanzo hasta el punto de poder buscar por cadenas exactas en el buscador de datasets  |
| Portillo Sánchez, Alonso | HH    | XX      | YY   | ZZ   | II     | Realizacion de FakeNodo, además de incluir la vista del perfil de usuario y el filtro avanzado en la bsuqueda de datasets |
| Sevillano Barea, Alejandro | 100    | 61      | 2769   | 9   | 16     | Construir un dataset seleccionando feature models y añadiendolos como si fuera un carrito y que se te descarguen automáticamente. Luego ese dataset se muestra en la lista de datasets. Realizacion de un dashboard para usuarios y para personas que no están registradas. |
| Espinosa Naranjo, Pablo  | HH    | XX      | YY   | ZZ   | II     | Realizacion de FakeNodo, ha incluido una serie de botones que permiten que cada dataset pueda ser valorado entre 1 a 5 estrellas modificando la base de datos para su incorporación  |
| Harana Mancilla, Rafael  | HH    | XX      | YY   | ZZ   | II     | Descripción breve  |
| **TOTAL**          | tHH   | tXX     | tYY  | tZZ  | tII    | Se han realizado 6 WI mas el FakeNodo, ademas de intentarse e implimentarse parte de otros 2  |


## Integración con otros equipos
Nombre-del-equipo: breve descripción de la integración

## Resumen ejecutivo (800 palabras aproximadamente)


## Descripción del sistema (1.500 palabras aproximadamente)


## Visión global del proceso de desarrollo (1.500 palabras aproximadamente)

El proceso de desarrollo sigue una estructura clara y organizada, para garantizar una colaboración eficiente, un historial de cambios limpio y un código estable.

### Principales Aspectos del Proceso
 - **Gestión de Commits:**

    - Se aplican los **estándares Conventional Commits**, asegurando que cada cambio sea atómico, claro y rastreable.
    - Los commits siguen la estructura **tipo(<área>): descripción breve**, donde los principales tipos incluyen feat, fix, docs, entre otros.
    - Se prohíben los mensajes genéricos o commits con código incompleto.
      
- **Gestión de Issues:**

    - Las tareas y problemas se gestionan mediante issues clasificados por **etiquetas** estándar (feature, bug, docs, etc.) y **priorizados** en high, medium o low.
    - Cada issue debe contar con una **descripción clara**, **responsable asignado** y un **flujo de trabajo** definido para su resolución.
    - Las tareas activas se organizan en el Project "Pescaito HUB" según su **estado**: Todo, In Progress, Staged, Done o Stopped.
      
- **Gestión de Ramas:**

    - La rama **main** refleja siempre el código estable y listo para producción, mientras que la rama develop se utiliza para integración de funcionalidades.
    - Las nuevas funcionalidades se desarrollan en ramas **feature/** específicas, y las versiones estables se gestionan mediante ramas **release/** siguiendo un esquema semántico (X.Y.Z).
    - Las ramas principales tienen **reglas de protección**, como la aprobación obligatoria de pull requests y la integración continua (CI) para validar cambios.
      
### Aplicación de las Políticas

Las políticas establecidas se han venido aplicando de manera progresiva en el proyecto, garantizando que todo el equipo siga un proceso estructurado y eficiente. Desde la gestión de commits atómicos, pasando por la correcta clasificación de issues, hasta la organización y protección de las ramas, todas las acciones se han alineado con las políticas definidas. Este enfoque ha permitido mejorar la calidad del código, la colaboración en equipo y el seguimiento de tareas, asegurando que cada parte del flujo de trabajo esté bien documentada y bajo control.

 ### Más Información
 
Para detalles completos sobre las políticas de gestión de commits, issues y ramas, consulta los documentos específicos alojados en la misma carpeta. 

## Entorno de desarrollo (800 palabras aproximadamente)

El desarrollo del proyecto se llevó a cabo en un entorno configurado de manera robusta y eficiente, con el objetivo de asegurar la reproducibilidad, estabilidad y facilidad de colaboración entre los miembros del equipo. A continuación, se describen los componentes esenciales del entorno y las herramientas utilizadas:

### Sistema Operativo y Configuración General
- **Sistema Operativo:** **Ubuntu 22.04 LTS**, utilizado de forma uniforme por todo el equipo para garantizar la compatibilidad.
- **Lenguaje de Programación:** **Python 3.10 o superior**, aprovechando las características modernas del lenguaje.
- **Framework Principal:** **Flask (versión 3.0.3)** como base para el desarrollo del backend.
- **Base de Datos:**
  - **MariaDB** para el entorno de producción y pruebas, con las bases de datos uvlhubdb y uvlhubdb_test.
  - **SQLite** como opción ligera para pruebas locales y desarrollo rápido.
- **Gestión de Dependencias:** Todas las dependencias se manejaron mediante el archivo **requirements.txt** para asegurar consistencia entre los diferentes entornos.

### Configuración de la Base de Datos
La base de datos MariaDB fue configurada siguiendo los pasos estándar de instalación y asegurando las credenciales necesarias:

**1. Instalación del servidor:**

```bash
sudo apt update
sudo apt install mariadb-server -y
sudo systemctl start mariadb
```

**2. Configuración inicial:**

Ejecutar la configuración segura:

```bash
sudo mysql_secure_installation
```

Valores predeterminados para una correcta instalación:

```bash
- Enter current password for root (enter for none): (enter)
- Switch to unix_socket authentication [Y/n]: `y`
- Change the root password? [Y/n]: `y`
    - New password: `uvlhubdb_root_password`
    - Re-enter new password: `uvlhubdb_root_password`
- Remove anonymous users? [Y/n]: `y`
- Disallow root login remotely? [Y/n]: `y` 
- Remove test database and access to it? [Y/n]: `y`
- Reload privilege tables now? [Y/n] : `y`
```

Crear las bases de datos necesarias:

```MariaDB
CREATE DATABASE uvlhubdb;
CREATE DATABASE uvlhubdb_test;
CREATE USER 'uvlhubdb_user'@'localhost' IDENTIFIED BY 'uvlhubdb_password';
GRANT ALL PRIVILEGES ON uvlhubdb.* TO 'uvlhubdb_user'@'localhost';
GRANT ALL PRIVILEGES ON uvlhubdb_test.* TO 'uvlhubdb_user'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

### Configuración del Proyecto
Sigue estos pasos para preparar el entorno de desarrollo:

**1. Clonar el repositorio**
```bash
git clone git@github.com:<USUARIO_GITHUB>/pescaito-hub.git
cd pescaito-hub
```

**2. Configurar entorno virtual**

Este paso es opcional si se prefiere usar un entorno virtual para la instalación de las dependencias:
```bash
sudo apt install python3.12-venv
python3.12 -m venv venv
source venv/bin/activate
```

**3. Instalar dependencias**
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

**4. Configurar variables de entorno**
```bash
cp .env.local.example .env
```

**5. Aplicar migraciones y poblar la base de datos**
```bash
flask db upgrade
rosemary db:seed
```

**6. Iniciar servidor de desarrollo**
```bash
flask run --host=0.0.0.0 --reload --debug
```

La aplicación estará disponible en: **http://localhost:5000.**

### Herramientas y Librerías Utilizadas

- **Frameworks y Librerías Principales:**
    - **Flask**: Framework principal para el desarrollo del servidor web.
    - **Flask-Login, Flask-WTF y Flask-SQLAlchemy:** Extensiones de Flask utilizadas para la autenticación, validación de formularios y manejo de bases de datos mediante ORM.
    - **SQLAlchemy**: Herramienta principal para la gestión de la base de datos.

- **Pruebas y Validación:**
    - **pytest y pytest-cov:** Herramientas para realizar pruebas unitarias y medir la cobertura del código.
    - **Selenium**: Utilizada para automatizar pruebas de interfaz de usuario.
    - **Locustfile**: Carga de datos para las pruebas

## Ejercicio de propuesta de cambio

## Conclusiones y trabajo futuro


https://github.com/EGCETSII/Entregables/wiki/Documento-del-proyecto
https://github.com/EGCETSII/Entregables/wiki/Modelo-de-portada

