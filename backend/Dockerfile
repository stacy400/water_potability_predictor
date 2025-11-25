FROM python:3.12-slimFROM python:3.11-slim



WORKDIR /appWORKDIR /app



COPY backend/app/requirements.txt .COPY backend/app/requirements.txt .

RUN pip install --no-cache-dir -r requirements.txtRUN pip install --no-cache-dir -r requirements.txt



COPY backend/app .COPY backend/app .

COPY backend/__init__.py /app/

CMD ["python", "main.py"]

ENV PYTHONUNBUFFERED=1
ENV PYTHONPATH=/app:$PYTHONPATH

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
