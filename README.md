# Publicar Marketplace

Este proyecto permite publicar productos en el Marketplace de Facebook de manera automatizada utilizando la API de Graph de Facebook. Está desarrollado en Node.js y proporciona una interfaz web para subir y gestionar productos.

## Características

- Publicación automática de productos en Facebook Marketplace
- Soporte para múltiples imágenes por producto
- Interfaz web para subir archivos CSV o Excel con productos
- Configuración segura de credenciales usando variables de entorno
- Validación de conexión con la API de Facebook

## Requisitos Previos

- Node.js (versión 14 o superior)
- Una página de Facebook con permisos para publicar en Marketplace
- Token de acceso de Facebook con permisos adecuados

## Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/rocioromera911/Publicar_Marketplace.git
   cd Publicar_Marketplace
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Configura las credenciales:
   - Copia el archivo `cred.env` y configura tus credenciales:
     ```
     PAGE_ID=TU_PAGE_ID
     ACCESS_TOKEN=TU_ACCESS_TOKEN
     ```

## Uso

### Probar Conexión

Ejecuta el script de prueba para verificar la conexión con Facebook:

```bash
node index.js
```

### Publicar Productos

1. Inicia el servidor web:
   ```bash
   npm start
   ```

2. Abre tu navegador en `http://localhost:3000`

3. Sube un archivo CSV o Excel con los productos a publicar

### Formato del Archivo CSV/Excel

El archivo debe contener las siguientes columnas:
- title: Título del producto
- description: Descripción del producto
- price: Precio del producto
- images: URLs de las imágenes (separadas por comas)

## Configuración

### Variables de Entorno

- `PAGE_ID`: ID de tu página de Facebook
- `ACCESS_TOKEN`: Token de acceso con permisos para publicar

### Obtener Credenciales de Facebook

1. Crea una aplicación en [Facebook Developers](https://developers.facebook.com/)
2. Obtén un token de acceso con permisos `pages_manage_posts`, `pages_show_list`
3. Configura el ID de tu página de Facebook

## Dependencias

- axios: Para hacer llamadas HTTP a la API de Facebook
- dotenv: Para manejar variables de entorno
- express: Framework web para Node.js
- multer: Middleware para subir archivos
- csv-parser: Para parsear archivos CSV
- xlsx: Para manejar archivos Excel

## Estructura del Proyecto

```
├── index.js          # Script principal de prueba
├── server.js         # Servidor web (si existe)
├── explicacion.txt   # Guía detallada de uso
├── package.json      # Configuración de Node.js
├── cred.env          # Archivo de credenciales (no subir a git)
├── uploads/          # Carpeta para archivos subidos
└── imagenes/         # Carpeta para imágenes
```

## Contribución

Si deseas contribuir a este proyecto:

1. Haz un fork del repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia ISC.

## Soporte

Si tienes problemas o preguntas, abre un issue en el repositorio de GitHub.