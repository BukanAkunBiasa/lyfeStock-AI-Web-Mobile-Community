# Menggunakan image Python sebagai base image
FROM python:3.9-slim

# Set working directory di dalam container
WORKDIR ai/Deployment

# Menyalin file requirements.txt untuk menginstal dependensi
COPY ai/Deployment/requirements.txt requirements.txt 

# Menginstal dependensi yang diperlukan
RUN pip install -r requirements.txt

# Menyalin seluruh kode aplikasi ke dalam container
COPY . .

# Menjalankan aplikasi Python
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=5000"]
