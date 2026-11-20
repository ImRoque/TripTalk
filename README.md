# TripTalk

TripTalk es una aplicación de escritorio tipo red social orientada a compartir recomendaciones de viaje y publicar ofertas de viajes organizados. Surgió como proyecto de la materia de Tópicos Avanzados de Programación y cuenta con una implementación principal en **Java (Swing)** y una versión paralela en **C# (Windows Forms)** que comparten el mismo esquema de datos en archivos JSON locales.

## Funcionalidades

- **Autenticación y roles**: Registro e inicio de sesión de usuarios con distinción entre cuenta estándar (`npc`) y administrador (`adm`).
- **Publicaciones de recomendación (`Opiniones`)**: Creación y consulta de reseñas sobre destinos visitados que incluyen presupuesto estimado, tres sitios recomendados, principal obstáculo del viaje, equipaje sugerido y mejores fechas para asistir.
- **Preguntas y respuestas**: Hilo de comentarios dentro de cada recomendación donde cualquier usuario puede hacer preguntas sobre el destino y recibir respuestas de otros viajeros.
- **Ofertas de viaje (`Viajes`)**: Publicación de paquetes o viajes con costo y detalles por parte de los administradores, permitiendo a los usuarios registrados marcar o retirar su interés (`Me interesa`).
- **Moderación (Java)**: Eliminación de publicaciones y preguntas, así como bloqueo y desbloqueo de cuentas de usuario (ocultando del feed el contenido de usuarios bloqueados).
- **Generación de reportes (Java)**:
  - **Lugares más populares (`.xlsx`)**: Conteo de los destinos con más menciones en publicaciones y preguntas, exportado a Excel con una gráfica de barras integrada.
  - **Interesados por viaje (`.xlsx`)**: Exportación a Excel del listado de usuarios interesados en una oferta de viaje específica.
  - **Top usuarios (`.pdf`)**: Documento PDF con la tabla de los tres usuarios con mayor cantidad de recomendaciones publicadas.

## Tecnologías

| Tecnología | Uso en el proyecto |
| :--- | :--- |
| **Java 21 / Swing** | Interfaz gráfica y lógica completa de la aplicación en `Java/TripTalk` (diseñada en NetBeans con `AbsoluteLayout` y componentes `edisoncorSX`). |
| **C# / Windows Forms (.NET Framework 4.7.2)** | Segunda implementación de escritorio en `C#/TripTalk` con las vistas de acceso, feed de publicaciones y comentarios. |
| **Gson y json-simple / Newtonsoft.Json** | Lectura y escritura de las entidades del sistema en archivos JSON. |
| **Apache POI (`poi-ooxml`)** | Creación de hojas de cálculo `.xlsx` y generación de gráficas de barras (`XDDFChart`) en la versión de Java. |
| **iText 7** | Generación del reporte `.pdf` de usuarios con más reseñas en la versión de Java. |
| **MySQL Workbench (`.mwb`)** | Modelo entidad-relación de referencia (`TripTalk.mwb`) incluido en la raíz del repositorio. |


