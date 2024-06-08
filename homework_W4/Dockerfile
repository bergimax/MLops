FROM agrigorev/zoomcamp-model:mlops-2024-3.10.13-slim
RUN pip install -U pip
RUN pip install pipenv

RUN pipenv install --system --deploy
EXPOSE 9696:9696
ENTRYPOINT ["gunicorn", "--bind=0.0.0.0:9696", "predict:app"]