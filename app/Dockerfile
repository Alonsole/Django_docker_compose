FROM python:3.10-alpine
ENV PYTHONDONTRITEBYTECODE="1"
ENV PYTHONBUFFERED="1"
WORKDIR /usr/src/app
ENV APP_HOME=/usr/src/app/web
RUN mkdir $APP_HOME
RUN mkdir $APP_HOME/static
COPY ./requirements.txt ./requirements.txt
RUN pip3 install -r requirements.txt
COPY . .
EXPOSE 8000

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]

