# disk image
FROM python:3.10-alpine

# Python dependencies
RUN apk update && apk add --no-cache \
    git \
    build-base \
    linux-headers \
    libffi-dev \
    openblas-dev \
    && pip install --upgrade pip

# install jax with GPU
RUN pip install "jax[cuda12]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html

# install veros
RUN pip install veros

# define workdir
WORKDIR /usr/src/app/

# start a bash terminal (for now...)
EXPOSE 3001
CMD ["sh"]

# execute veros
# ...
