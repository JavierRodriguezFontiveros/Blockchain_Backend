# Blockchain_Backend

# 🚀 Blockchain Portal Backend

## 📌 Descripción
Este proyecto es un backend para un portal blockchain que permite gestionar wallets, realizar transacciones, simular una blockchain y ejecutar contratos inteligentes. Está construido utilizando **Spring Boot**, **JPA**, **Docker** y otras tecnologías clave para asegurar robustez y escalabilidad.

## 🏗️ Arquitectura del Proyecto
El backend está compuesto por varios módulos que trabajan en conjunto:

- **Autenticación y Gestión de Sesiones**: Manejo de registro, login y sesiones de usuario.
- **Gestión de Wallets**: Creación, actualización y sincronización del saldo de wallets.
- **Transacciones**: Envío y recepción de fondos entre wallets.
- **Simulación de Blockchain**: Validación y almacenamiento de transacciones en bloques.
- **Firma Digital**: Uso de criptografía para garantizar la seguridad de las transacciones.
- **Contratos Inteligentes**: Ejecución de contratos en un entorno simulado.

## 📂 Estructura del Repositorio

```
📦 blockchain-portal-backend
├── 📁 src
│   ├── 📁 main
│   │   ├── 📁 java/com/hackathon/blockchain
│   │   │   ├── 📁 config        # Configuración del proyecto
│   │   │   ├── 📁 controller    # Endpoints de la API REST
│   │   │   ├── 📁 model         # Clases de modelo (Wallet, Transaction, Block...)
│   │   │   ├── 📁 repository    # Interfaces de acceso a la base de datos
│   │   │   ├── 📁 service       # Lógica de negocio y procesamiento de datos
│   │   │   ├── 📁 util          # Utilidades y helpers
│   ├── 📁 test  # Tests unitarios y de integración
├── 📜 Dockerfile   # Configuración del contenedor
├── 📜 docker-compose.yml  # Orquestación con Docker
├── 📜 application.yml  # Configuración de Spring Boot
├── 📜 README.md  # Documentación del proyecto
```

## ⚙️ Tecnologías Utilizadas

- **Java 17** + **Spring Boot**: Framework principal
- **Spring Security**: Autenticación y autorización
- **JPA (Hibernate)**: Gestión de base de datos
- **PostgreSQL**: Base de datos relacional
- **Docker**: Contenedorización
- **WebSockets**: Comunicación en tiempo real
- **Cryptography API**: Firma digital

## 🛠️ Instalación y Configuración

### 1️⃣ Prerrequisitos

- Docker y Docker Compose instalados
- Java 17 instalado

### 2️⃣ Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/blockchain-portal-backend.git
cd blockchain-portal-backend
```

### 3️⃣ Levantar el entorno con Docker
```bash
docker-compose up --build
```

### 4️⃣ Acceder a la API
Una vez iniciado, el backend estará disponible en: `http://localhost:8080`

## 🔗 Endpoints Principales

### 🏠 Autenticación
| Método | Endpoint | Descripción |
|--------|---------|-------------|
| POST | `/auth/register` | Registro de usuario |
| POST | `/auth/login` | Inicio de sesión |

### 💰 Wallets
| Método | Endpoint | Descripción |
|--------|---------|-------------|
| GET | `/wallets/{id}` | Obtener detalles de una wallet |
| POST | `/wallets` | Crear una nueva wallet |

### 💸 Transacciones
| Método | Endpoint | Descripción |
|--------|---------|-------------|
| POST | `/transactions` | Crear una transacción |
| GET | `/transactions/{id}` | Obtener detalles de una transacción |

### ⛓️ Blockchain
| Método | Endpoint | Descripción |
|--------|---------|-------------|
| GET | `/blocks` | Obtener todos los bloques |
| POST | `/blocks/mine` | Minar un nuevo bloque |

## 🔒 Seguridad
- Uso de JWT para autenticación
- Protección de endpoints con Spring Security
- Cifrado de datos sensibles

## 🧪 Pruebas
Ejecutar los tests con:
```bash
mvn test
```

## 📌 Futuras Mejoras
- Implementación de un explorador de bloques
- Integración con redes blockchain reales (Ethereum, Bitcoin)
- Soporte para contratos inteligentes en Solidity

## 📜 Licencia
Este proyecto está bajo la licencia MIT. ¡Siéntete libre de contribuir! 🚀
