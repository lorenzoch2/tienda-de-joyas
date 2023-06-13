## Tienda de Joyas

Este es un proyecto de una tienda de joyas que proporciona endpoints para obtener joyas y aplicar filtros a la consulta de joyas. Utiliza una base de datos PostgreSQL y se implementa utilizando Express.js.

### Instalación

Sigue los siguientes pasos para ejecutar el proyecto en tu máquina local:

1. Clona este repositorio o descarga los archivos en tu equipo.
2. Asegúrate de tener PostgreSQL instalado y en ejecución.
3. Crea una base de datos llamada "joyas" en PostgreSQL.
4. Ejecuta el script `tienda-de-joyas.sql` en la base de datos "joyas" para crear la tabla "inventario" y agregar algunos datos de ejemplo.
5. Abre una terminal y navega hasta el directorio del proyecto.
6. Ejecuta el siguiente comando para instalar las dependencias del proyecto:

   npm install

7. Una vez que se hayan instalado las dependencias, ejecuta el siguiente comando para iniciar el servidor:

   npm run dev

8. El servidor se iniciará en el puerto 3000. Puedes acceder a la tienda de joyas a través de la siguiente URL:

   http://localhost:3000

### Endpoints

La tienda de joyas proporciona los siguientes endpoints:

- `GET /joyas`: Devuelve un listado de joyas. Puedes agregar parámetros de consulta para limitar la cantidad de resultados, ordenarlos y paginarlos. Ejemplo de uso:

  http://localhost:3000/joyas?limits=3&page=2&order_by=stock_ASC

- `GET /joyas/filtros`: Devuelve un listado de joyas filtradas según los parámetros de consulta proporcionados. Los filtros disponibles son: precio máximo, precio mínimo, categoría y metal. Ejemplo de uso:

  http://localhost:3000/joyas/filtros?precio_min=25000&precio_max=30000&categoria=aros&metal=plata


### Estructura de archivos

- `consultas.js`: Contiene las consultas a la base de datos para obtener joyas y joyas filtradas, así como la preparación del formato HATEOAS.
- `index.js`: Archivo principal del servidor Express que define los endpoints y middleware.
- `tienda-de-joyas.sql`: Script SQL para crear la base de datos "joyas", la tabla "inventario" y agregar datos de ejemplo.
- `package.json`: Archivo de configuración de npm que contiene las dependencias y scripts del proyecto.

### Dependencias

- Express.js: Framework web utilizado para la creación del servidor y la definición de los endpoints.
- nodemon: Herramienta utilizada para reiniciar automáticamente el servidor cuando se realizan cambios en los archivos.
- pg: Librería de Node.js para interactuar con PostgreSQL.

### Autor

Este proyecto fue desarrollado por Lorenzo Chacano como una muestra de implementación de una tienda de joyas utilizando Express.js y PostgreSQL.

Si tienes alguna pregunta o sugerencia, no dudes en contactarme. ¡Disfruta explorando la tienda de joyas!
