FROM python:3.10
ENV PYTHONUNBUFFERED 1
RUN pip install --upgrade pip
WORKDIR /app
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --requirement /app/requirements.txt
COPY . /app
EXPOSE 5000
CMD python server.py