## 🔧 Servicios

### 🧠 `scheduler`
- Servicio que escucha en el puerto `8989`.
- Se construye desde el directorio `./scheduler`.
- Depende del servicio `database`.

### 🛍️ `storefront`
- Servicio frontend expuesto en los puertos `7575` (HTTP) y `1443` (HTTPS).
- Se construye desde el directorio `./storefront`.
- Depende del servicio `database`.

### 🗄️ `database`
- Contenedor de MySQL basado en la imagen oficial `mysql:latest`.
- Usa un archivo `.env` con variables de entorno localizado en `./mysql/env_vars`.
- Monta el volumen persistente `kineteco` para los datos de la base de datos.
- Ejecuta scripts de inicialización si existen en `./mysql`.
