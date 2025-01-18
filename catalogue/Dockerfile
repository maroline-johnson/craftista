FROM python:latest
WORKDIR /app
COPY /catalogue .
RUN pip install -r requirements.txt
CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:5000"]