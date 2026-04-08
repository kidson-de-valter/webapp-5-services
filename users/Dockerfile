FROM python:3.11-slim

# 1. Instalar certificados CA (CRÍTICO)
RUN apt-get update && \
    apt-get install -y ca-certificates curl && \
    update-ca-certificates

WORKDIR /app

# 2. Atualizar pip
RUN pip install --upgrade pip

# 3. Instalar dependências Python
RUN pip install fastapi uvicorn --no-cache-dir

# 4. Copiar código
COPY app .

# 5. Executar serviço
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]