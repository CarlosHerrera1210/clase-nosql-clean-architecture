# Clase NoSQL — Clean Architecture imperativa

Proyecto base de la actividad, generado con el plugin Clean Architecture de Bancolombia. Usa Java 21, Spring Boot y Spring MVC (REST imperativo); no utiliza Spring WebFlux.

## Requisitos

- Java JDK 21 o posterior.
- Gradle 9.2.1 o posterior. El proyecto incluye Gradle Wrapper 9.8.2, por lo que puedes ejecutar sus tareas sin instalar Gradle globalmente.

## Ejecutar la aplicación

En PowerShell, desde la carpeta del repositorio, inicia la aplicación con:

```powershell
.\gradlew.bat bootRun
```

Prueba el endpoint GET en:

```text
http://localhost:8080/api/usecase/path
```

El controlador `ApiRest` responde inicialmente `Value from use case v1`. Se encuentra en `infrastructure/entry-points/api-rest/src/main/java/co/com/bancolombia/api/ApiRest.java`.

Detén la aplicación con `Ctrl+C` en la terminal.

## Compilar y generar cobertura

```powershell
.\gradlew.bat build jacocoMergedReport
```

## Estructura

- `applications/app-service`: aplicación Spring Boot y configuración.
- `domain/model`: modelos y contratos del dominio.
- `domain/usecase`: casos de uso.
- `infrastructure/entry-points/api-rest`: API REST imperativa con Spring MVC.
- `deployment`: configuración para despliegue.

## Comandos útiles

```powershell
.\gradlew.bat tasks
.\gradlew.bat build
```
