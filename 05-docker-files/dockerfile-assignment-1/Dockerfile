# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.
from node:6-alpine

EXPOSE 3000 

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install 

RUN npm cache clean --force

COPY . .

CMD [ "/sbin/tini", " --","node","./bin/www" ]
