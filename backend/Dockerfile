
FROM python:3.10-slim

# working directory
WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt

# Make port 80 available
EXPOSE 80

ENV NAME World

# Run app.py
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
