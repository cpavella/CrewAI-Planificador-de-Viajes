FROM python:3.12-slim

WORKDIR /app

RUN pip install --no-cache-dir uv

COPY . .

RUN uv sync --no-dev

ENV PYTHONUNBUFFERED=1

CMD ["sh", "-c", "uv run python -m uvicorn backend_proyecto_planificador_de_viajes.main:app --app-dir ./src --host 0.0.0.0 --port ${PORT:-8080}"]