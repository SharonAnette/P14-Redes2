# Práctica 14 — Protocolo HTTP

## Objetivo
Realizar un servidor HTTP que busque ejecutar las operaciones de tipo GET y POST.

## Cómo funciona
La práctica consiste en implementar un servidor HTTP básico utilizando Node.js, que permite manejar solicitudes GET y POST desde clientes web.

1. **Configuración del servidor:** Se crea un servidor con el módulo `http` de Node.js, escuchando en el puerto 3000.  
2. **Procesamiento de solicitudes:**  
   - En una solicitud **GET** a la ruta `/get`, el servidor obtiene los parámetros enviados en la URL y responde en formato JSON.  
   - En una solicitud **POST** a la ruta `/post`, el servidor recopila los datos enviados en el cuerpo de la petición, los interpreta y los devuelve como respuesta JSON.  
3. **Control de rutas:** Si la solicitud no corresponde a `/get` ni a `/post`, el servidor responde con un error 404 indicando que la ruta no existe.  

El servidor implementa un modelo cliente-servidor simple, utilizando el protocolo HTTP sobre TCP/IP, demostrando la estructura de comunicación de la web y la gestión de métodos de solicitud básicos. 
---

# Práctica 15 — Ejemplo Protocolo HTTP en C

## Objetivo
Desarrollar un servidor HTTP básico en lenguaje C para ilustrar el funcionamiento fundamental del protocolo HTTP, aceptando conexiones en el puerto 80, procesando solicitudes de clientes y respondiendo con una página HTML simple.

## Cómo funciona
El servidor se implementa utilizando **sockets TCP** para establecer una conexión confiable entre cliente y servidor.

1. **Creación del socket:** Se configura un socket TCP (`AF_INET`, `SOCK_STREAM`) enlazado al puerto 80.  
2. **Escucha y aceptación de conexiones:** El servidor entra en modo de escucha (`listen`) y acepta conexiones entrantes (`accept`).  
3. **Envío de respuesta HTTP:** Al recibir una solicitud, el servidor responde con un encabezado HTTP estándar y una página HTML que incluye un mensaje de bienvenida y un botón interactivo que muestra la fecha y hora actual.  
4. **Cierre de conexión:** Una vez enviada la respuesta, el socket se cierra para atender nuevas solicitudes.

Esta práctica demuestra la estructura básica del protocolo HTTP y la comunicación entre cliente y servidor a nivel de red utilizando el lenguaje C.  
