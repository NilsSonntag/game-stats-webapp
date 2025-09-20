# Dev only image for now
FROM ghcr.io/astral-sh/uv:python3.13-trixie-slim

WORKDIR /app

# Copy from the cache instead of linking since it's a mounted volume (see compose)
ENV UV_LINK_MODE=copy

# Copy and install dependencies
COPY pyproject.toml uv.lock ./
RUN --mount=type=cache,target=/root/.cache/uv \
    uv sync --locked --no-install-project

ENV PATH="/app/.venv/bin:$PATH"

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
