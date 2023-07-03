FROM {{service_python_image}}

WORKDIR /app

COPY requirements.txt requirements.txt

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

RUN apk update && apk add tk

COPY drone_management .

CMD ["python", "-u", "drone_management.py"]