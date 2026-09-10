FROM python:3.10-slim

WORKDIR /app

COPY Pipfile Pipfile.lock ./

RUN pip install pipenv && \
    pipenv install --system --deploy

COPY . .

EXPOSE 5000

CMD ["python", "-m", "flask", "--app", "__init__:app", "run", "--host=0.0.0.0", "--port=5000"]