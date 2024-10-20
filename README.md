
# Scraper de Productos de Amazon

Este proyecto es un scraper web construido usando [Puppeteer](https://pptr.dev/) y [xlsx](https://www.npmjs.com/package/xlsx) para extraer detalles de productos desde una página de resultados de búsqueda de Amazon y exportarlos en un archivo Excel.

## Características

- Extrae títulos de productos y precios de Amazon.
- Maneja la paginación, moviéndose automáticamente a la siguiente página hasta que no haya más páginas disponibles.
- Exporta los datos extraídos a un archivo Excel (`products.xlsx`).

## Requisitos Previos

Asegúrate de tener instalados Node.js y npm. También necesitarás instalar las bibliotecas Puppeteer y xlsx.

1. Instalar [Node.js](https://nodejs.org/)
2. Instalar los paquetes necesarios:
   ``` bash
   npm install puppeteer xlsx
   ```

## Configuración

1. Clona este repositorio o copia el código en tu proyecto.
2. Instala las dependencias:
   ```bash
   npm install
   ```

## Uso

Para ejecutar el scraper, utiliza el siguiente comando:

```bash
node index.js
```

### Configuración

Puedes configurar las siguientes opciones:

- **URL**: Modifica la constante `URL` en el script para apuntar a diferentes páginas de resultados de búsqueda de Amazon.
- **Proxy (Opcional)**: Puedes añadir un proxy al script descomentando las líneas relacionadas con el proxy y especificando tu URL de proxy, nombre de usuario y contraseña.

### Ejemplo de Salida

El script extraerá los títulos y precios de los productos de la página de Amazon y los guardará en un archivo Excel llamado `products.xlsx` en el directorio actual.

### Notas

- Puppeteer está configurado actualmente para iniciarse en modo **headful** (no headless) con Firefox como navegador. Puedes cambiar a Chrome o ejecutar el script en modo headless modificando las opciones de `launch`.
- El script maneja la paginación haciendo clic en el botón "Siguiente" hasta que llegue a la última página.

## Dependencias

- [Puppeteer](https://pptr.dev/) - Una biblioteca de Node.js que proporciona una API de alto nivel para controlar Chrome o Firefox a través del protocolo DevTools.
- [xlsx](https://www.npmjs.com/package/xlsx) - Una biblioteca para leer/escribir archivos Excel en JavaScript.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
