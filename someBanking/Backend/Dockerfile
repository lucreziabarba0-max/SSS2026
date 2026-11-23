
FROM python
WORKDIR /app

RUN apt-get update && apt-get install -y git

RUN git clone https://github.com/mmenapace/SomeBankingApp.git .

RUN pip install -r backend/requirements.txt

WORKDIR /app/backend

ENTRYPOINT ["python", "-m", "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]