# 1. Build stage
FROM python:3.11-slim AS builder
WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 2. Runtime stage
FROM python:3.11-alpine
WORKDIR /app

COPY --from=builder /usr/local /usr/local
COPY . .

# create non-root user
RUN adduser -D appuser
USER appuser

# healthcheck (adjust port per service)
HEALTHCHECK CMD curl --fail http://localhost:8000/health || exit 1

CMD ["python", "main.py"]