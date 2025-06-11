# Ejercicio Clase 3 módulo 3 Bootcamp DevOps
## Grupo
- Grupo 3
- Integrantes:
    - Eduardo Abarca
    - Fabián
    - María
    - Juan Pablo
- Fecha: 10-06-2025

## Descripción del proyecto

**Ejercicio Guiado: Automatización Profesional con Maven**

En este ejercicio vas a trabajar como si fueras parte
del equipo de desarrollo de “TaskMaster”, una
herramienta simple que gestiona tareas desde
consola. Aprenderás a automatizar el ciclo de
construcción del proyecto usando Maven, una
herramienta ampliamente usada en la industria.

Objetivos
● Comprender qué es Maven y cómo automatiza la
construcción del software.
● Instalar y configurar Maven en tu equipo.
● Crear un proyecto con estructura profesional.
● Agregar dependencias externas y gestionar
versiones.
● Crear y ejecutar pruebas unitarias.
● Empaquetar la aplicación como .jar lista para
distribución.

Preguntas finales
- ¿Qué aprendiste sobre el ciclo de vida de Maven?
- ¿Cómo facilita Maven el trabajo en equipo y la reproducibilidad?
- ¿Cuál fue el mayor reto al trabajar con dependencias?
- ¿Por qué crees que Maven es tan usado en entornos empresariales?
- ¿Qué harías diferente si tuvieras que automatizar otro proyecto?

## Comandos usados (Maven)

## 🛠️ Comandos usados con Maven

A continuación, algunos de los comandos utilizados durante el desarrollo:

```bash
# Generar proyecto con estructura estándar
mvn archetype:generate -DgroupId=com.equipo.taskmaster -DartifactId=taskmaster

# Compilar el proyecto
mvn clean compile

# Ejecutar la aplicación principal (requiere exec-maven-plugin)
mvn exec:java -Pdev

# Ejecutar los tests
mvn test

# Empaquetar el proyecto como .jar
mvn package

```

## Dependencias y plugins utilizados
### Dependencias
- junit:junit:4.13.2 – Para pruebas unitarias básicas
- org.apache.commons:commons-lang3:3.12.0 – Utilidades de Apache Commons

### Plugins
- maven-compiler-plugin – Para compilar el código Java
- exec-maven-plugin – Para ejecutar la clase principal desde Maven
- maven-surefire-plugin – Para correr pruebas unitarias
- maven-jar-plugin – Para empaquetar la app como un .jar

## Mayor aprendizaje técnico

Nuestro mayor aprendizaje fue entender cómo Maven gestiona todo el ciclo de vida del proyecto, desde la compilación hasta las pruebas y el empaquetado, incluyendo la gestión de perfiles para distintos entornos (dev, prod).

Aprendimos a:

- Organizar un proyecto Java con la estructura estándar de Maven.
- Agregar dependencias sin descargarlas manualmente.
- Ejecutar la aplicación desde Maven usando plugins.
- Leer propiedades definidas por perfiles (env.name) desde el código Java.

## Mayor desafío enfrentado
El mayor desafío fue configurar correctamente los perfiles y entender cómo funcionan las propiedades (-D), especialmente al ejecutarlas desde PowerShell, ya que la sintaxis puede romper la ejecución si no se usa correctamente.

También enfrentamos dificultades iniciales al gestionar múltiples versiones de plugins y resolver errores relacionados con la duplicación del maven-compiler-plugin.


## Cómo ejecutar el proyecto

1. Clona el repositorio
```bash
git clone https://github.com/EdoAbarca/taskmaster.git
cd taskmaster
```

2. Compilar el proyecto
```bash
mvn clean compile
```

3. Ejecutar en entorno de desarrollo
```bash
mvn exec:java -Pdev
```
O en producción:
```bash
mvn exec:java -Pprod
```
