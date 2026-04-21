FROM python:3.11-slim

WORKDIR /app/backend-server

COPY . .

RUN pip install -r requirements.txt
RUN pip install certifi

EXPOSE 8080

CMD ["python", "server.py"]
