# Use an official Python image as a base
FROM python:3.10-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt .
# RUN pip install --no-cache-dir -r requirements.txt

RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt


# Copy application files (if any)
COPY . .

# Expose the default ChromaDB port
EXPOSE 8000

# # Run ChromaDB server
# CMD ["chromadb", "run", "--host", "0.0.0.0", "--port", "8000"]

# CMD ["python", "-m", "chromadb", "run", "--host", "0.0.0.0", "--port", "8000"]

# CMD ["python", "-c", "import chromadb; chromadb.HttpServer().run(host='0.0.0.0', port=8000)"]

# CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]


# CMD ["uvicorn", "chromadb.app:server", "--host", "0.0.0.0", "--port", "8000"]
