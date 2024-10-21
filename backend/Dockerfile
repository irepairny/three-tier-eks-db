FROM python

WORKDIR /app

RUN apt-get update -y \
    && apt-get install -y python3-pip python3-dev default-libmysqlclient-dev pkg-config \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY . .

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["flask", "run", "--host", "0.0.0.0"]

 
