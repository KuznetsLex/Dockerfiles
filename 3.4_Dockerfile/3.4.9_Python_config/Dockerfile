FROM python:3.9
WORKDIR /app
RUN apt-get update && \ 
	apt-get install -y curl && \ 
	rm -rf /var/lib/apt/lists/*
RUN pip install flask
COPY config.ini script.py ./
ENV LOG_LEVEL=info APP_MODE=production
EXPOSE 9000
ENTRYPOINT ["python", "script.py"]
