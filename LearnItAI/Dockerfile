# Use official lightweight Python image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy requirements first
COPY requirements.txt .

# Install dependencies
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copy the rest of the app
COPY . .

# Expose port 8000 (or whichever port your app uses)
EXPOSE 8000

# Run your app (change app.py if your entry file has a different name)
CMD ["python", "app.py"]
