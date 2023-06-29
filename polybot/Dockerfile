FROM python:3.9
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
# Expose the port (if needed)
# EXPOSE <port_number>
ENV TOKEN_FILE_PATH /app/.telegramToken
CMD ["python", "app.py"]
