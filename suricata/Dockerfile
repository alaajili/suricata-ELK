# Use a base image, for instance, Ubuntu
FROM ubuntu:latest

# Update package lists and install necessary dependencies

RUN apt-get update && apt-get upgrade -y && \
apt-get install -y software-properties-common && \
add-apt-repository ppa:oisf/suricata-stable && \
apt-get update && \
apt-get install -y suricata

# Copy Suricata configuration files (adjust paths as needed)
# COPY suricata.yaml /etc/suricata/suricata.yaml

# Set the entry point
CMD ["suricata", "-c", "/etc/suricata/suricata.yaml", "--init-errors-fatal"]
