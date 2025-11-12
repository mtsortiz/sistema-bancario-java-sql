# 🏦 Sistema Bancario Java SQL

<div align="center">
  <h2>💰 Sistema Bancario Completo 💰</h2>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white" alt="Maven"/>
  <img src="https://img.shields.io/badge/MVC-FF6B6B?style=for-the-badge&logo=architecture&logoColor=white" alt="MVC"/>
</div>

## 📋 Descripción
Sistema bancario completo desarrollado en Java utilizando el patrón arquitectónico MVC (Model-View-Controller). El sistema permite la gestión integral de cuentas bancarias, transacciones, clientes y operaciones financieras con persistencia en base de datos SQL.

## ✨ Características
- 💳 **Gestión de cuentas:** Creación, consulta y administración de cuentas bancarias
- 💸 **Transacciones:** Depósitos, retiros, transferencias entre cuentas
- 👥 **Gestión de clientes:** Registro y administración de información de clientes
- 🔐 **Seguridad:** Sistema de autenticación y autorización de usuarios
- 📊 **Reportes:** Generación de reportes financieros y estados de cuenta
- 💾 **Persistencia:** Base de datos SQL para almacenamiento de información
- 🖥️ **Interfaz gráfica:** GUI desarrollada con Java Swing

## 🏛️ Arquitectura
El proyecto implementa el patrón **MVC (Model-View-Controller)**:
- 📊 **Model:** Entidades del dominio bancario y lógica de negocio
- 👁️ **View:** Interfaz gráfica de usuario (Java Swing)
- 🎮 **Controller:** Controladores para manejar la interacción entre Vista y Modelo

## 🛠️ Tecnologías Utilizadas
- **Lenguaje:** Java 8
- **Base de datos:** SQL (MySQL/PostgreSQL)
- **Interfaz gráfica:** Java Swing
- **Persistencia:** JDBC
- **Build tool:** Maven
- **Testing:** JUnit

## Estructura del Proyecto
```
sistema-bancario-java-sql/
├── cfg/                      # Archivos de configuración
│   ├── conexionBD.properties    # Configuración de base de datos
│   ├── config.properties        # Configuración general
│   └── usuarios.properties      # Configuración de usuarios
├── sql/                      # Scripts de base de datos
│   ├── banco.sql               # Estructura de la base de datos
│   └── datos.sql               # Datos de prueba
├── src/main/java/            # Código fuente
│   └── banco/                # Paquete principal
├── src/main/resources/       # Recursos
├── images/                   # Recursos gráficos
└── pom.xml                   # Configuración Maven
```

## 🚀 Funcionalidades Principales

### 💳 Gestión de Cuentas
- Apertura de cuentas corrientes y de ahorro
- Consulta de saldos y movimientos
- Cierre de cuentas
- Actualización de información de cuentas

### 💰 Operaciones Bancarias
- 📈 **Depósitos:** Ingreso de dinero a cuentas
- 📉 **Retiros:** Extracción de fondos con validación de saldo
- 🔄 **Transferencias:** Movimiento de fondos entre cuentas
- 🔍 **Consultas:** Verificación de saldos y historial

### ⚙️ Administración
- Gestión de clientes y sus datos personales
- Control de usuarios del sistema
- Generación de reportes
- Auditoría de transacciones

## Requisitos del Sistema
- **Java:** JDK 8 o superior
- **Base de datos:** MySQL 5.7+ o PostgreSQL 9.6+
- **Memoria:** 1 GB RAM mínimo
- **Sistema operativo:** Windows, macOS, Linux

## Instalación y Configuración

### 1. Base de Datos
1. Instalar MySQL o PostgreSQL
2. Crear la base de datos ejecutando `sql/banco.sql`
3. Cargar datos de prueba con `sql/datos.sql`

### 2. Configuración
Editar los archivos de configuración en `cfg/`:
- `conexionBD.properties`: Configurar conexión a la base de datos
- `config.properties`: Parámetros generales del sistema
- `usuarios.properties`: Usuarios del sistema

### 3. Compilación
```bash
mvn clean compile
```

### 4. Ejecución
```bash
mvn exec:java -Dexec.mainClass="banco.Main"
```

## Configuración de Base de Datos
Ejemplo de configuración en `cfg/conexionBD.properties`:
```properties
db.url=jdbc:mysql://localhost:3306/banco
db.username=usuario
db.password=contraseña
db.driver=com.mysql.cj.jdbc.Driver
```

## Testing
Ejecutar las pruebas unitarias:
```bash
mvn test
```

## Seguridad
- Autenticación de usuarios mediante credenciales
- Validación de permisos por rol
- Encriptación de contraseñas
- Logs de auditoría para todas las transacciones

## Casos de Uso Principales
1. **Login de usuario**
2. **Consulta de saldo**
3. **Realizar depósito**
4. **Realizar retiro**
5. **Transferencia entre cuentas**
6. **Generar estado de cuenta**
7. **Administrar clientes**

## Diagrama de Clases
El sistema incluye las siguientes entidades principales:
- `Cliente`: Información personal del cliente
- `Cuenta`: Cuenta bancaria (corriente/ahorro)
- `Transaccion`: Registro de operaciones
- `Usuario`: Usuario del sistema
- `Banco`: Entidad principal del sistema

## Contribución
Para contribuir al proyecto:
1. Fork del repositorio
2. Crear rama para nueva funcionalidad
3. Implementar siguiendo el patrón MVC
4. Agregar tests unitarios
5. Actualizar documentación
6. Enviar pull request

## Licencia
Este proyecto es para fines educativos y de demostración del patrón MVC en sistemas bancarios.
