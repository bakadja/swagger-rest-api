FROM python:3-alpine

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/
RUN pip3 install --no-cache-dir -r requirements.txt

# Vérifiez les modules installés
RUN pip3 list

# Vérifiez l'installation de connexion
RUN python3 -c "import connexion; print('connexion module imported successfully')"

COPY . /usr/src/app
EXPOSE 8080

ENTRYPOINT ["python3"]
CMD ["-m", "swagger_server"]