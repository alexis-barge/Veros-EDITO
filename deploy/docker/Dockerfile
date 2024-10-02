# disk image
FROM ubuntu:20.04  

# Python dependencies
RUN apt-get update && apt-get install -y \
    python3-pip python3-dev git

# install jax with GPU
RUN pip install --upgrade pip && \
    pip install "jax[cuda12]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html

# install veros
RUN pip install veros

# define workdir
WORKDIR /usr/src/app/

# start veros
EXPOSE 80
CMD ["veros", "copy-setup", "acc"]

CMD ["sleep", "infinity"]
