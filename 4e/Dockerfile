# Usa una imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia los archivos de dependencias
COPY requirements.txt .

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Copia el código de la aplicación
COPY app.py .

# Crea un usuario no root para ejecutar la aplicación
RUN adduser --disabled-password --gecos '' usertest

# Cambia al nuevo usuario
USER usertest

# Expone el puerto 5000
EXPOSE 5000
#Ejecutar la aplicacion 
# Comando para ejecutar la aplicación
CMD ["python", "app.py"]