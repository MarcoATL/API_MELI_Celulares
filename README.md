# API_MELI_Celulares
Servicio que muestra el top 1000 de celulares con menor precio utilizando la API de Mercado Libre

# Proyecto de API para Consultar Precios de Celulares en Mercado Libre

Este proyecto es una API desarrollada en Node.js que consulta los precios de celulares en Mercado Libre y devuelve el top 1000 de artículos con menor precio, incluyendo información relevante sobre el vendedor y las condiciones del artículo.

## Estructura del Proyecto

- **app.js**: Archivo principal que contiene la lógica de la API. Este archivo configura el servidor Express y define las rutas y la lógica para interactuar con la API de Mercado Libre.
- **get.js**: Archivo auxiliar (si existe) que puede contener funciones o lógica específica para obtener datos.
- **test_api_structure.js**: Archivo utilizado para realizar pruebas de estructura de la respuesta de la API de Mercado Libre, ayudando a comprender cómo están organizados los datos.
- **package.json**: Archivo que define las dependencias del proyecto y los scripts de npm.
- **package-lock.json**: Archivo que asegura la integridad de las dependencias instaladas.
- **.env**: Archivo de configuración para variables de entorno (asegúrate de que esté correctamente configurado y no lo compartas públicamente).
- **node_modules/**: Directorio generado por npm que contiene todas las dependencias del proyecto.

## Requisitos

- **Node.js** (v14 o superior)
- **npm** (v6 o superior)

## Instalación

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git

2. Navega al directorio del proyecto:
    ```bash
    cd nombre-del-proyecto
3. Instala las dependencias necesarias:
 ```bash
npm install
  ```
## Ejecución del Proyecto

Para ejecutar el proyecto, sigue estos pasos:

1. Asegúrate de que tienes configuradas las variables de entorno necesarias en el archivo `.env`.

2. Inicia el servidor:

   ```bash
   node app.js
3. Accede a la API desde tu navegador o herramienta de prueba de API en la siguiente URL:
  http://localhost:3000/top-1000-lowest-price

## Descripción de la API

### Ruta: `/top-1000-lowest-price`
- **Método**: `GET`
- **Descripción**: Devuelve un listado con el top 1000 de artículos con menor precio relacionados con la búsqueda "celular" en Mercado Libre.
- **Respuesta**: Un JSON que incluye los siguientes campos para cada artículo:
  - `seller_id`: ID del vendedor.
  - `seller_name`: Nombre del vendedor.
  - `brand`: Marca del artículo.
  - `free_shipping`: Indica si el envío es gratuito (`true` o `false`).
  - `logistics_type`: Tipo de logística utilizado para el envío.
  - `seller_location`: Ubicación del vendedor (ciudad y estado).
  - `condition`: Condición del artículo (nuevo, usado, etc.).
  - `price_range`: Rango de precio del artículo en MXN.
