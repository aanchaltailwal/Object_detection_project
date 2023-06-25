FROM python:3.9
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY app.py .
COPY static static
COPY templates templates
EXPOSE 8082
ENV YOLO_URL=http://detect-service:8081
ENV MONGO_URL=mongodb://mongo-db:27017
CMD ["python", "app.py"]



