# Utilisez une image officielle Python
FROM python:3.9-slim

# Définir le dossier de travail
WORKDIR /app

# Copier les fichiers nécessaires
COPY app.py ./
COPY index.html ./templates/

# Installer Flask
RUN pip install Flask

# Exposer le port 80
EXPOSE 80

# Démarrer l'application Flask
CMD ["python", "app.py"]
