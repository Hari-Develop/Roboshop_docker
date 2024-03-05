FROM python:3.9.18-alpine3.19
EXPOSE 8080
ENV AMQP_USER=Roboshop \
    AMQP_PASS=Roboshop123
USER root
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt
COPY *.py /app/
COPY payment.ini /app/
CMD ["uwsgi" , "--ini" , "payment.ini"]