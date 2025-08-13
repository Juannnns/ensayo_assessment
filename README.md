
# 📌 Sistema de Gestión de Datos Financieros

## Descripción:
 Este sistema resuelve el problema de gestionar datos financieros desorganizados provenientes de plataformas como Nequi y Daviplata, almacenados en múltiples archivos Excel. 

## Funcionalidades:
 - Normalización (1FN, 2FN, 3FN)
- Base de datos MySQL relacional
 - Carga masiva desde CSV
 - API CRUD en Express.js
 - Dashboard en Vite
- Consultas SQL avanzadas


## 🚀 Tecnologías Utilizadas
 - Frontend: Vite@latest
 - Backend: Express.js
 - Base de datos: MySQL
 - Driver: mysql2
 - Procesamiento CSV: csv-parser


## 1️⃣ Clonar repositorio

```
git clone https://github.com/Juannnns/financial-data-system.git
```

## 2️⃣ Instalar dependencias del backend

```
npm install express mysql2 csv-parser
```

## 3️⃣ Instalar dependencias del frontend

```
npm install vite@lastest
```


## 📊 Normalización de la Base de Datos
- 1FN: eliminar grupos repetidos y asegurar valores atómicos
-  2FN: eliminar dependencias parciales de claves compuestas
- 3FN: eliminar dependencias transitivas


## 📥 Carga Masiva desde CSV
El archivo .xlsx original se convierte a .csv y se procesa con csv-parser para insertarlo en la base de datos.

## 🖥 API CRUD
 Funciones:
 - Crear: Agregar registros
 - Leer: Obtener datos
 - Actualizar: Modificar registros existentes
- Eliminar: Borrar registros


## 📌 Consultas Avanzadas (ejecutar desde Postman):
1. Total pagado por cliente
 2. Facturas pendientes con datos de cliente y transacción
 3. Transacciones por plataforma (Nequi, Daviplata)


## 4️⃣ Iniciar backend
```
node server.js 
```


##5️⃣ Iniciar frontend
```
npm run dev
```

## 👤 Información del Desarrollador
Nombre: Juan José 
Clan: Tayrona 
Correo: juanbarrios0956@gmail.ckm
