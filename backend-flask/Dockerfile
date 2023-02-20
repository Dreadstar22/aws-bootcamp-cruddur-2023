FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside the container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# Contains the Python to install to run app
COPY requirements.txt requirements.txt

# Inside Container
# Install Python libraries used for app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means everything in the current directory
# first period . - /backend-flask (outside container)
# second period . - /backend-flask (inside container)
COPY . .

# Set Environment Variables (Env Vars)
# Inside Container remain set when container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]