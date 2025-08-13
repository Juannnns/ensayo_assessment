
###############################################################################
# 📌 Sistema de Gestión de Datos Financieros
#
# Descripción:
# Este sistema resuelve el problema de gestionar datos financieros
# desorganizados provenientes de plataformas como Nequi y Daviplata,
# almacenados en múltiples archivos Excel. 
# 
# Funcionalidades:
# - Normalización (1FN, 2FN, 3FN)
# - Base de datos MySQL relacional
# - Carga masiva desde CSV
# - API CRUD en Express.js
# - Dashboard en Vite
# - Consultas SQL avanzadas
###############################################################################

echo "📢 Iniciando instalación del Sistema de Gestión de Datos Financieros..."

###############################################################################
# 🚀 Tecnologías Utilizadas
# - Frontend: Vite@latest
# - Backend: Express.js
# - Base de datos: MySQL
# - Driver: mysql2
# - Procesamiento CSV: csv-parser
###############################################################################

###############################################################################
# 1️⃣ Clonar repositorio
###############################################################################
echo "🔽 Clonando repositorio..."
git clone https://github.com/tuusuario/financial-data-system.git
cd financial-data-system || { echo "❌ Error: No se pudo acceder al proyecto"; exit 1; }

###############################################################################
# 2️⃣ Instalar dependencias del backend
###############################################################################
echo "📦 Instalando dependencias del backend..."
cd backend || exit
npm install express mysql2 csv-parser

###############################################################################
# 3️⃣ Instalar dependencias del frontend
###############################################################################
echo "📦 Instalando dependencias del frontend..."
cd ../frontend || exit
npm install vite

###############################################################################
# 📊 Normalización de la Base de Datos
# 1FN: eliminar grupos repetidos y asegurar valores atómicos
# 2FN: eliminar dependencias parciales de claves compuestas
# 3FN: eliminar dependencias transitivas
###############################################################################

###############################################################################
# 4️⃣ Configurar la base de datos
###############################################################################
echo "🛠 Creando base de datos..."
cd .. || exit
mysql -u root -p < scripts/create_db.sql

###############################################################################
# 📥 Carga Masiva desde CSV
# El archivo .xlsx original se convierte a .csv y se procesa con csv-parser
# para insertarlo en la base de datos.
###############################################################################
echo "📥 Importando datos desde CSV..."
node scripts/import_csv.js

###############################################################################
# 🖥 API CRUD
# Funciones:
# - Crear: Agregar registros
# - Leer: Obtener datos
# - Actualizar: Modificar registros existentes
# - Eliminar: Borrar registros
###############################################################################

###############################################################################
# 📌 Consultas Avanzadas (ejecutar desde Postman):
# 1. Total pagado por cliente
# 2. Facturas pendientes con datos de cliente y transacción
# 3. Transacciones por plataforma (Nequi, Daviplata)
###############################################################################

###############################################################################
# 5️⃣ Iniciar backend
###############################################################################
echo "🚀 Iniciando backend..."
cd backend || exit
node server.js &

###############################################################################
# 6️⃣ Iniciar frontend
###############################################################################
echo "🌐 Iniciando frontend..."
cd ../frontend || exit
npm run dev

###############################################################################
# 📷 Modelo Relacional
# Guardado en: model/relational_model.png
###############################################################################

###############################################################################
# 👤 Información del Desarrollador
# Nombre: Tu Nombre
# Clan: Tu Clan
# Correo: tu.email@example.com
###############################################################################

echo "✅ Sistema de Gestión de Datos Financieros instalado y ejecutándose."