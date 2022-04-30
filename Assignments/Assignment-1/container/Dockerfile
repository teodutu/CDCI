FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y python3-pip
RUN pip3 install slo-generator==2.0.0

# So that you can modify exploit.py inside the container
RUN apt-get install -y vim

COPY exploit.yaml /root
COPY run_exploit.sh /root
RUN chmod +x /root/run_exploit.sh
