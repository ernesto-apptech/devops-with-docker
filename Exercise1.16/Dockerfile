FROM ubuntu

WORKDIR /app

EXPOSE 8080

# Installing cURL.
RUN apt update && apt upgrade -y; apt install curl -y

# Installing node and NPM
RUN curl -sL https://deb.nodesource.com/setup_20.x | bash
RUN apt install -y nodejs

RUN npm install -g http-server
COPY . .
RUN npm i
RUN npm run build

# And finally the command to run the application
CMD [ "http-server", "dist" ]