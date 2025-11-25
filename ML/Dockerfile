FROM python:3.12-slim

WORKDIR /app

COPY ML/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY ML .

ENV PYTHONUNBUFFERED=1

CMD ["python", "train.py"]
