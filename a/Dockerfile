FROM python:3.10

WORKDIR /app
ENTRYPOINT ["/app/entrypoint.py"]

COPY poetry.lock pyproject.toml ./
RUN pip install poetry==1.8.5 \
 && poetry config virtualenvs.create false \
 && poetry install

COPY . ./
RUN chmod +x /app/entrypoint.py
