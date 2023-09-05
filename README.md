# Resilience4j 
Resilience4j es una biblioteca de Java para implementar patrones de tolerancia a fallos y gestión de resiliencia en aplicaciones.
Uno de los patrones que veremos en este repositorio es el patron Circuit Breaker(interruptor de circuito):
Simulando fallas y latencia 
Personalizando parametro del Circuit Breaker y criterios por defecto
Timeout
Llamadas lentas
Configurando Resilience4j con extension application.yml
Anotación @CircuitBreaker
Anotacion @Timelimiter
Implementando fallBackMethod 
Spring Cloud Gateway con Resilience4j


Este microservicio está diseñado para gestionar información relacionada con productos y sus respectivos ítems en una aplicación para asi administrar los datos asociados a estos elementoses y su implementación de un 'circuit breaker'
![image](https://github.com/joanvasquez21/microservices-producto-items-circuitbreaker/assets/70104624/231c2d25-9372-4f01-9eab-f966b6cdfcfb)

1.- Para implementar Circuit breaker añadimos en el servicio items la version 2.5.3 en mi caso porque tenia una version mas antigua y habilitamos la dependencia Resilience4j
```
<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
	    <version>2.3.12.RELEASE</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>

<dependency> 
      <groupId>org.springframework.cloud</groupId> 
      <artifactId>spring-cloud-starter-circuitbreaker-resilience4j</artifactId> 
</dependency>
```
2.- 
