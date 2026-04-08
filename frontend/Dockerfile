FROM nginx:alpine

ENV HTTP_PROXY=http://proxy:8000
ENV HTTPS_PROXY=http://proxy:8000
# 1. Instalar certificados CA (CRÍTICO)
RUN apt-get update && \
    apt-get install -y ca-certificates curl && \
    update-ca-certificate

COPY index.html /usr/share/nginx/html/index.html