# Proyecto Eureka Server

## Descripción

Este proyecto implementa un **Eureka Server** utilizando Spring Boot y Spring Cloud Netflix. El servidor Eureka actúa como un registro de servicios centralizado (Service Registry), permitiendo que otros microservicios se registren y sean descubiertos dinámicamente dentro de un sistema distribuido basado en microservicios.

## Configuración del Proyecto

### Archivo `application.properties`
La configuración básica del servidor Eureka es la siguiente:

```properties
server.port=8761
spring.application.name=eureka-server

eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
```

#### Detalle de configuraciones:
- `server.port=8761`: Define el puerto en el que se levanta el servidor Eureka.
- `spring.application.name=eureka-server`: Nombre de la aplicación para identificar el servidor dentro del ecosistema de servicios.
- `eureka.client.register-with-eureka=false`: Evita que el servidor Eureka se registre a sí mismo.
- `eureka.client.fetch-registry=false`: Deshabilita la búsqueda de registros de otros servidores Eureka (configuración ideal para un servidor independiente).

## Tecnologías utilizadas
- **Spring Boot 2.7.15**: Framework para facilitar la configuración y el arranque del proyecto.
- **Spring Cloud Netflix Eureka**: Implementación del servidor de registro.
- **Java 1.8**: Lenguaje de programación utilizado.
- **Maven**: Herramienta de gestión de dependencias.

## Ejecución del Proyecto

1. Clona el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   ```

2. Compila y ejecuta el proyecto:
   ```bash
   mvn spring-boot:run
   ```

3. Accede al servidor Eureka mediante la URL:
   ```
   http://localhost:8761
   ```

En esta interfaz, podrás visualizar los servicios registrados una vez que otros microservicios se conecten al servidor.

## Notas finales

El servidor Eureka es una pieza fundamental en una arquitectura de microservicios, permitiendo el descubrimiento dinámico y mejorando la resiliencia del sistema. Este proyecto utiliza configuraciones básicas para levantar un servidor funcional que puede ser integrado en aplicaciones distribuidas.

