# Clase NoSQL — Clean Architecture con WebFlux

Proyecto base de la actividad para generar una aplicación Java con Clean Architecture y Spring WebFlux usando el plugin de Bancolombia.

## Requisitos

- Java JDK 21 o posterior.
- Gradle 9.2.1 o posterior. El proyecto incluye Gradle Wrapper 9.8.2, así que no necesitas instalar Gradle globalmente.

## Ejecutar el proyecto

Abre PowerShell en la carpeta del repositorio y ejecuta:

```powershell
.\gradlew.bat bootRun
```

Cuando la aplicación esté iniciada, consulta el endpoint:

```text
http://localhost:8080/api/usecase/path
```

La respuesta inicial es una cadena vacía. Para cambiarla, edita la clase `Handler` en `infrastructure/entry-points/reactive-web/src/main/java/co/com/bancolombia/api/Handler.java`.

Para detener la aplicación, usa `Ctrl+C` en la terminal.

## Compilar y generar cobertura

```powershell
.\gradlew.bat build jacocoMergedReport
```

## Estructura general

- `applications/app-service`: punto de entrada y configuración de Spring Boot.
- `domain/model`: modelos del dominio.
- `domain/usecase`: casos de uso.
- `infrastructure/entry-points/reactive-web`: rutas HTTP y handlers WebFlux.
- `deployment`: archivos para despliegue.

## Comandos útiles

```powershell
.\gradlew.bat tasks
.\gradlew.bat build
```