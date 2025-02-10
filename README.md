# 🚀 TKambio Full Solution

Este proyecto utiliza `docker-compose` para orquestar tres servicios. Sigue los pasos a continuación para configurar y ejecutar el entorno correctamente.

## 📦 Requisitos

Asegúrate de tener instalados los siguientes componentes en tu máquina:

- [Git](https://git-scm.com/downloads)
- [Docker](https://www.docker.com/get-started) (versión 26.1.1 o superior recomendada)
- [Docker Compose](https://docs.docker.com/compose/install/) (versión v2.27.0-desktop.2 o superior recomendada)

## 🔧 Instalación y ejecución

Sigue estos pasos para clonar el repositorio, actualizar los submódulos y levantar los servicios con `docker-compose`:

```bash
# 1️⃣ Clonar el repositorio principal
git clone https://github.com/Pieromental/tkambio_full_solution.git

# 2️⃣ Entrar en el directorio del proyecto
cd tkambio_full_solution

# 3️⃣ Inicializar y actualizar los submódulos
git submodule update --init --recursive

# 4️⃣ Obtener la última versión de los submódulos
git submodule update --recursive --remote

# 5️⃣ Construir y ejecutar los contenedores en segundo plano
docker-compose up -d --build
```

## 📂 Estructura del Proyecto

```
tkambio_full_solution/
├── nginx.conf
├── tkambio_back/   # Backend
├── tkambio_challenge_front/  # Frontend principal
├── tkambio_challenge_static_front/  # Frontend estático
├── .gitmodules
├── docker-compose.yml
└── README.md
```

## 🔗 Repositorios de cada módulo

- Backend: [tkambio_back](https://github.com/Pieromental/tkambio_back.git)
- Frontend principal: [tkambio_challenge_front](https://github.com/Pieromental/tkambio_challenge_front.git)
- Frontend estático: [tkambio_challenge_static_front](https://github.com/Pieromental/tkambio_challenge_static_front.git)

## 🛠️ Comandos útiles

### 🚀 Detener y eliminar los contenedores
```bash
docker-compose down
```

### 🔄 Reiniciar los servicios con cambios recientes
```bash
docker-compose up -d --build
```

### 🛑 Ver logs de los contenedores
```bash
docker-compose logs -f
```

---
_Hecho con ❤️ por [Pieromental](https://github.com/Pieromental)._

