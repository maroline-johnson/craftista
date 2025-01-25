FROM python:3
WORKDIR /app
COPY /catalogue .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:5000"]