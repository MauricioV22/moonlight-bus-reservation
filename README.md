# Moonlight — Sistema de reservas de autobuses

Moonlight es una aplicación web desarrollada para gestionar reservas de viajes en autobús en Guanacaste, Costa Rica.

El sistema permite consultar rutas, seleccionar viajes y asientos, registrar reservaciones y generar boletos digitales con código QR.

> Este repositorio funciona como portafolio del proyecto.  
> El código fuente completo se mantiene en un repositorio privado.

---

## Funcionalidades

- Consulta de rutas y horarios.
- Selección y control de asientos.
- Registro de reservaciones.
- Almacenamiento de información en Firestore.
- Generación automática de boletos en PDF.
- Generación de códigos QR.
- Envío de boletos por correo electrónico.
- Formulario de comentarios, sugerencias y reportes.
- Interfaz web para el proceso de reserva.
- Mapa interactivo con geolocalización y trazado de rutas.

---

## Tecnologías

**Backend**
- Java 17
- Spring Boot
- Spring MVC

**Base de datos**
- Firebase Firestore

**Frontend**
- HTML
- CSS
- JavaScript
- Thymeleaf

**Servicios y herramientas**
- Firebase Admin SDK
- JavaMail
- iText PDF
- ZXing QR
- Maven
- Git / GitHub
- Leaflet
- CARTO Basemaps
- OpenStreetMap
- OSRM
- Esri World Imagery
---

## Flujo general

```text
Usuario
   ↓
Interfaz web
   ↓
Spring Boot
   ↓
Reserva y validación de asientos
   ↓
Firestore
   ↓
Generación de boleto PDF + QR
   ↓
Envío del boleto por correo
```
---

## Mapa interactivo y trazado de rutas

Moonlight incluye un mapa interactivo para visualizar las paradas disponibles y calcular recorridos desde la ubicación del usuario hasta un destino seleccionado.

El módulo fue desarrollado con **Leaflet** e integra distintos servicios de mapas y rutas:

- **CARTO Basemaps** para el mapa base en modo oscuro.
- **OpenStreetMap** como mapa alternativo.
- **Esri World Imagery** para la vista satelital.
- **OSRM** para calcular y dibujar rutas entre el usuario y las paradas.
- Geolocalización del navegador para obtener la ubicación actual.
- Agrupación de marcadores cuando existen varias paradas cercanas.
- Búsqueda de lugares y selección de destinos directamente desde el mapa.

El sistema también muestra información aproximada del recorrido, como distancia, duración y hora estimada de llegada.

### Vista del mapa

<img width="1917" height="978" alt="Mapa interactivo de Moonlight" src="https://github.com/user-attachments/assets/629afd1f-3713-430c-b0e8-3b53dfda34a3" />
<img width="1917" height="982" alt="Vista satelital de las paradas" src="https://github.com/user-attachments/assets/24021f05-e158-4c24-aed9-6aadf5f8a3b7" />
<img width="1917" height="977" alt="Paradas disponibles en el mapa" src="https://github.com/user-attachments/assets/fb42b7c1-f15d-44dc-b623-e154c223b891" />


### Ejemplo de recorrido

<img width="1917" height="977" alt="Ruta calculada desde la ubicación del usuario" src="https://github.com/user-attachments/assets/323f6139-a9b4-4a69-9463-d414089f266f" />
<img width="1917" height="980" alt="Recorrido hacia una parada de Moonlight" src="https://github.com/user-attachments/assets/1b39fe03-6ec8-443d-a3be-ab5573dfffda" />
<img width="1917" height="980" alt="Información de distancia y duración del viaje" src="https://github.com/user-attachments/assets/2a2bbceb-9b23-4c40-a5d6-eeea35c45630" />


---

## Capturas

### Página principal

<img width="1901" height="980" alt="Página principal de Moonlight" src="https://github.com/user-attachments/assets/4977b0d2-d03b-45c7-8892-348f81962588" />
<img width="1896" height="980" alt="Página principal de Moonlight" src="https://github.com/user-attachments/assets/d74a4dc4-1a74-44b1-bc10-c04ebe2e93c4" />
<img width="1897" height="977" alt="Página principal de Moonlight" src="https://github.com/user-attachments/assets/c136910f-63a4-4d0d-aafe-55d4f19643c6" />


### Selección de rutas
<img width="1900" height="978" alt="Selección de rutas" src="https://github.com/user-attachments/assets/22227798-857a-4936-ab7b-cee7e5efee5b" />
<img width="1901" height="981" alt="Selección de rutas" src="https://github.com/user-attachments/assets/4eccca74-31e0-46db-bad0-47fb1d34557e" />
<img width="1901" height="980" alt="Selección de rutas" src="https://github.com/user-attachments/assets/e5290f84-9557-4a5a-b917-f73219a60725" />
<img width="1901" height="978" alt="Selección de rutas" src="https://github.com/user-attachments/assets/2f23d9cc-a2ec-46c3-8555-834c5cb9475a" />



### Selección de asientos

<img width="1917" height="977" alt="Selección de asientos" src="https://github.com/user-attachments/assets/090e766c-48f6-4040-861b-8f8589fa6a49" />


### Proceso de reserva
<img width="1905" height="977" alt="Formulario de reserva" src="https://github.com/user-attachments/assets/4bdac574-5933-4ffe-9c07-e500fc4165c0" />
<img width="1901" height="980" alt="Formulario de reserva" src="https://github.com/user-attachments/assets/130212a1-9f66-409d-b30e-5420e3156f3d" />

<img width="1917" height="978" alt="Formulario de reserva" src="https://github.com/user-attachments/assets/723dd1cb-9c40-4d5d-895d-271ce74ed61d" />


### Boleto generado

<img width="1118" height="491" alt="Boleto generado" src="https://github.com/user-attachments/assets/4009814c-c0db-4dab-bf62-48eee43861ac" />
[Ver boleto de ejemplo en PDF](https://github.com/user-attachments/files/32675839/boleto_22_4fa42e2e-625b-4560-9c26-4c942e2a7502.pdf)
<img width="1807" height="981" alt="Boleto generado" src="https://github.com/user-attachments/assets/b5063f97-889f-47c6-ae62-1d00cbe71c27" />


---
## Arquitectura

Moonlight utiliza una arquitectura web basada en Spring Boot.

El backend gestiona la lógica de reservaciones, disponibilidad de asientos, persistencia de datos, generación de boletos y comunicación con servicios externos.

**Firebase Firestore** se utiliza para almacenar las reservaciones y controlar la disponibilidad de los asientos.

El módulo de mapas utiliza **Leaflet** como base e integra servicios externos como **CARTO, OpenStreetMap, Esri y OSRM** para visualización, geolocalización y cálculo de recorridos.

---

## Estado del proyecto

Proyecto funcional desarrollado originalmente como proyecto académico y posteriormente ampliado con nuevas funcionalidades.

Actualmente cuenta con:

- Sistema de reservaciones funcional.
- Persistencia de datos con Firestore.
- Control de disponibilidad de asientos.
- Generación de boletos PDF.
- Generación de códigos QR.
- Envío de boletos por correo electrónico.
- Gestión de comentarios, sugerencias y reportes.
- Mapa interactivo con geolocalización y trazado de rutas.

---

## Código fuente

El código fuente completo de Moonlight se mantiene en un repositorio privado.

Este repositorio público contiene únicamente documentación, capturas y material demostrativo del proyecto.

---

## Autor

**Mauricio Vargas Ramos**

Estudiante de Ingeniería en Sistemas Computacionales  
Enfoque principal: desarrollo backend

[LinkedIn](https://www.linkedin.com/in/mauricio-vargas-58979238b/)

---

© 2026 Mauricio Vargas Ramos. All rights reserved.






