
FROM python:3.11-slim

WORKDIR /app

RUN apt-get update && apt-get install -y --no-install-recommends ca-certificates \
    && rm -rf /var/lib/apt/lists/*

COPY netfree-ca.crt /usr/local/share/ca-certificates/netfree-ca.crt
RUN update-ca-certificates

COPY requirements.txt .
RUN pip install --cert /usr/local/share/ca-certificates/netfree-ca.crt --no-cache-dir -r requirements.txt
COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]
