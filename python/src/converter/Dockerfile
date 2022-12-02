# FROM python:3.10
# ENV PYTHONUNBUFFERED 1
# RUN pip install --upgrade pip
# WORKDIR /app
# COPY ./requirements.txt /app
# RUN pip install --no-cache-dir --requirement /app/requirements.txt
# COPY . /app
# EXPOSE 8080
# CMD python server.py

FROM python:3.10-slim-bullseye

RUN apt-get update \
  && apt-get install -y --no-install-recommends --no-install-suggests \
  build-essential ffmpeg \
  && pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --requirement /app/requirements.txt
COPY . /app

CMD ["python3", "consumer.py"]