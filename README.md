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

4. **Verificar que los contenedores estén corriendo**

```bash
docker ps
```

Deberías ver los contenedores activos listados.

5. **Ver logs de un contenedor (opcional)**

Para revisar la salida de un contenedor específico (por ejemplo, llamado `web`):

```bash
docker logs -f web
```

6. **Detener los contenedores**

Cuando quieras parar el entorno:

```bash
docker-compose down
```


---

## Notas adicionales

- Si haces cambios en el Dockerfile o en la configuración, recuerda reconstruir las imágenes con `docker compose build`.
- Los puertos expuestos y volúmenes están configurados en el archivo `docker-compose.yml`.
- Para más información sobre Docker y Docker Compose, visita la [documentación oficial](https://docs.docker.com/).
