# Deployment Guide

## Prerequisites
- Docker Desktop running
- 8GB+ RAM
- Git installed

## Deployment
```bash
cd /path/to/data_engineering_takehome1
docker compose -f ./docker-compose.yml --project-name my_assesment up -d
docker ps  # Verify: master, worker1, worker2, jupyter, docs
```

## Access
- **Spark UI:** http://localhost:8080
- **Jupyter:** http://localhost:8888

## Cleanup
```bash
docker compose -f ./docker-compose.yml --project-name my_assesment down -v
```

**Repo:** https://github.com/Shibiraj/data_engineering_takehome1


## Recommended Workflow

1. **Development:** Use Jupyter Notebook for initial development
2. **Testing:** Convert notebook to `.py` script and test with spark-submit
3. **Production:** Deploy with spark-submit in automated pipeline
