# Usar una imagen base de Python
FROM python:3.9

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar los archivos de la aplicación al contenedor
COPY . /app

# Instalar las dependencias necesarias
RUN pip install --no-cache-dir -r requirements.txt

# Exponer el puerto 5000 para Gunicorn
EXPOSE 5000

# Comando para ejecutar Gunicorn (servidor de la app)
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5000", "app:app"]
