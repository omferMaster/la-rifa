RifaApp
🌟 Presentación
RifaApp es una aplicación web desarrollada en React con TypeScript que permite gestionar la venta de rifas de manera sencilla y organizada. La app muestra un tablero con 100 números disponibles, donde los usuarios pueden registrar su nombre y teléfono en un puesto, verificar el estado del pago y exportar los registros a un archivo Excel.

🏠 Características
Interfaz interactiva para seleccionar números.

Registro de participantes con nombre y teléfono.

Marcado de pagos realizados.

Exportación de registros en formato Excel.

Búsqueda rápida por nombre.

⚙️ Tecnologías Utilizadas
Frontend: React + TypeScript + TailwindCSS

Backend: Node.js con Express y PostgreSQL

Librerías Adicionales:

XLSX para exportación de datos

lucide-react para iconos

🛠️ Instalación y Configuración
1. Clonar el Repositorio
bash
Copiar
Editar
git clone https://github.com/tuusuario/RifaApp.git
cd RifaApp
2. Instalación de Dependencias
Ejecuta el siguiente comando para instalar todas las dependencias necesarias:

bash
Copiar
Editar
npm install
📊 Configuración del Servidor
1. Configurar PostgreSQL
Asegúrate de tener PostgreSQL instalado y crea una base de datos llamada rifadb.

Dentro de PostgreSQL, ejecuta:

sql
Copiar
Editar
CREATE TABLE registros (
    id SERIAL PRIMARY KEY,
    number VARCHAR(2) UNIQUE NOT NULL,
    nombre VARCHAR(255) NOT NULL,
    telefono VARCHAR(20) NOT NULL,
    pago BOOLEAN DEFAULT FALSE
);
2. Configurar Variables de Entorno
Crea un archivo .env en la raíz del backend y agrega:

env
Copiar
Editar
DATABASE_URL=postgres://usuario:password@localhost:5432/rifadb
PORT=5000
3. Iniciar el Servidor Backend
bash
Copiar
Editar
cd backend
npm install
node server.js
El servidor estará corriendo en http://localhost:5000.

🌟 Ejecutar la Aplicación
En otra terminal, ejecuta el siguiente comando para levantar el frontend:

bash
Copiar
Editar
npm run dev
La aplicación estará disponible en http://localhost:3000.

🚀 Uso
Abre la aplicación en tu navegador.

Selecciona un número disponible.

Ingresa los datos del participante.

Marca el pago cuando corresponda.

Usa la búsqueda para encontrar un registro rápidamente.

Descarga la lista de registros en Excel.

🛠️ Contribución
Si deseas contribuir, haz un fork del repositorio, crea una rama con tus cambios y envía un pull request.

📃 Licencia
Este proyecto está bajo la licencia MIT.