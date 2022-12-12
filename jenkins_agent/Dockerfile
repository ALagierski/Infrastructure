ARG DEBIAN_FRONTEND=noninteractive
FROM jenkins/ssh-agent:4.2.1-jdk11
USER root
RUN apt-get update && apt-get install -y curl python3 python3-pip unzip ansible git
RUN groupadd -g 997 docker && usermod -aG docker jenkins
RUN curl -fsSL https://get.docker.com | sh
RUN curl -SL https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose
RUN curl https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip -o awscliv2.zip && unzip awscliv2.zip && ./aws/install -i /usr/local/aws-cli -b /usr/local/bin
