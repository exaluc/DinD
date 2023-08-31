FROM almalinux:8

LABEL fr.erz.author="Lucian BLETAN" \
      description="DinD AlmaLinux 8"

RUN dnf -y update && \
    dnf -y install dnf-plugins-core && \
    dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo && \
    dnf -y install docker-ce docker-ce-cli containerd.io python3-pip && \
    dnf clean all

RUN curl -L "https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64" -o /usr/local/bin/docker-compose && \
    chmod +x /usr/local/bin/docker-compose

ENTRYPOINT ["dockerd"]
