FROM python:slim
# RUN pip --version
# RUN echo ls -alt
WORKDIR /app
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . /app
VOLUME /app/data
ENTRYPOINT [ "./docker-entrypoint.sh" ]
EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0"]
