FROM node:16.17

LABEL maintainer="Fabiano F. Stoffel <ffpthai@gmail.com>"

WORKDIR /usr/src/app

# para caso seja necessário aguardar alguma dependência subir [passos no docker-compose]
# RUN apt update && apt install -y netcat wget
# RUN wget -q -O /usr/bin/wait-for https://raw.githubusercontent.com/eficode/wait-for/v2.2.3/wait-for && \
#     chmod +x /usr/bin/wait-for
# Instalar git caso container não tenha+
# RUN apt install -y git
# Parear o id com o usuário da máquina "real" para evitar problemas de permissão. Consultar com cat /etc/passwd
# RUN usermod -u 1001 node

# Signed Commit
RUN apt update && \
    apt install --no-install-recommends -y gpg gnupg gpg-agent socat

USER node

EXPOSE 3000

CMD [ "tail", "-f", "/dev/null" ]
