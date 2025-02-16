# Guía de Configuración

## Requisitos

Antes de comenzar, asegúrate de que los siguientes requisitos estén instalados:

- Docker Desktop 4.15+
- WSL2 activado

## Pasos de Instalación

1. Clona este repositorio:
    ```bash
    git clone https://github.com/tu-repositorio.git
    ```

2. Accede a la carpeta del repositorio:
    ```bash
    cd bigdata-env
    ```

3. Ejecuta Docker Compose para iniciar los servicios:
    ```bash
    docker-compose up -d
    ```

4. Verifica que los contenedores estén corriendo:
    ```bash
    docker-compose ps
    ```

5. Accede a Jupyter Lab en tu navegador en [http://localhost:8888](http://localhost:8888).

6. Ejecuta los scripts de prueba:
    - Prueba de Spark: `python scripts/test_spark.py`
    - Verificación de conexiones: `bash scripts/check_connections.sh`

## Problemas Comunes y Soluciones

- **WSL2 no inicia**: Ejecuta `wsl --set-default-version 2` en PowerShell como administrador.
- **Docker no responde**: Asegúrate de que Docker Desktop esté corriendo y que la opción "Linux Engine" esté activada.

## Diagrama de Arquitectura



## Resultados de Validación

| Servicio       | Tiempo de Respuesta |
|----------------|---------------------|
| PostgreSQL     | <100ms              |
| MongoDB        | <100ms              |
| Redis          | <5ms                |
| Spark          | <10 segundos        |

