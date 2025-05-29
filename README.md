# Proyecto Docker Compose + Flask + Apache (HTTPS) - Instrucciones para iniciar

Este repositorio contiene la configuración para levantar el entorno usando Docker y Docker Compose.

---

## Requisitos previos

- Tener instalado [Docker](https://docs.docker.com/get-docker/)
- Tener instalado [Docker Compose](https://docs.docker.com/compose/install/)

---

## Pasos para iniciar el entorno con Docker

1. **Clonar el repositorio**

```bash
git clone https://github.com/UAO-AFRG/Parcial-3.git
```

2. **Construir las imágenes Docker**

Ejecuta el siguiente comando para construir las imágenes definidas en el `Dockerfile` y `docker-compose.yml`:

```bash
docker-compose build
```

3. **Levantar los contenedores**

Para iniciar los contenedores en segundo plano (detached mode):

```bash
docker compose up -d
```

