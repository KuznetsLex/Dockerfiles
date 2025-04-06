FROM python:3.9
WORKDIR /app
RUN pip install Flask Werkzeug==2.2.2.
COPY app.py /app/
EXPOSE 8000
ENTRYPOINT ["python","app.py"]