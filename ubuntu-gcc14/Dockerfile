FROM ubuntu:oracular-20240617

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt update && \
	apt install gcc -y && \
	apt install openjdk-17-jdk -y && \
	apt install gradle -y
