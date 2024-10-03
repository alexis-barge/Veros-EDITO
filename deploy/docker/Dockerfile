# disk image
FROM ubuntu:20.04  

# Python dependencies
RUN apt-get update && apt-get install -y \
    python3-pip python3-dev git

# install jax with GPU
RUN pip install --upgrade pip && \
    pip install "jax[cuda12]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html

# Install Veros
RUN pip install veros

# Define workdir
WORKDIR /usr/src/app/

# Copy the ACC setup for Veros
RUN veros copy-setup acc

# Expose port (if necessary, depending on Veros usage)
EXPOSE 80

# Run the simulation
CMD ["veros", "run", "acc/acc.py"]
