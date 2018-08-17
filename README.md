# Dev-RK
Docker image to set up dev environment for RescueKerala

To build the image (from the directory containing the docker file):
> docker build -t image-name .

To run the image :
> docker run --rm -it -p 8000:8000 image-name /bin/bash

From the shell do the following steps:
1) /etc/init.d/postgresql start
2) cp .env.example .env
3) python3 manage.py migrate
4) python3 manage.py collectstatic
5) python3 manage.py runserver

