# Use an official lightweight Python image.
FROM python:3.12-slim

# Set the working directory in the container.
WORKDIR /app

# Copy requirements.txt and install dependencies.
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code.
COPY sudoku_ms.py .

# Expose the port the app runs on.
EXPOSE 8000

# Run the FastAPI app with Uvicorn.
CMD ["uvicorn", "sudoku_ms:app", "--host", "0.0.0.0", "--port", "8000"]
