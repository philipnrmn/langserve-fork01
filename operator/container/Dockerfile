FROM python:3.11-bookworm

ADD src /usr/src/server

WORKDIR /usr/src/server
RUN pip install .

EXPOSE 8000
ENV OPENAI_API_KEY=missing
CMD ["python", "server.py"]
