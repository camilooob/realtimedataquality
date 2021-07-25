# Use the official lightweight Python image.
# https://hub.docker.com/_/python
FROM python:3.7-slim
RUN mkdir src
ENV APP_HOME /src
WORKDIR $APP_HOME
RUN pip install jupyter
CMD jupyter notebook --no-browser --ip=0.0.0.0 --port=8888 --allow-root



# Copy local code to the container image.
# ENV APP_HOME /app
# WORKDIR $APP_HOME
# COPY . ./

# Install production dependencies.
# RUN pip install -r requirements.txt
# RUN export DOCKER_CLIENT_TIMEOUT=1200
# RUN export COMPOSE_HTTP_TIMEOUT=1200
# Run the web service on container startup. Here we use the gunicorn
# webserver, with one worker process and 8 threads.
# For environments with multiple CPU cores, increase the number of workers
# to be equal to the cores available.
#CMD exec gunicorn --preload --bind :$PORT --workers 1 --worker-class uvicorn.workers.UvicornWorker  --threads 8 main:app --timeout 1200Z