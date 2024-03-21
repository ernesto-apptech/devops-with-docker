# We need JAVA 8
FROM ubuntu:latest

EXPOSE 5000

WORKDIR /usr/src/app

# Installing cURL.
RUN apt update && apt upgrade -y; apt install curl -y


# Installing node and NPM
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

# Copy all of the source code
COPY . .

# Building the project
RUN NODE_ENV=development npm i
RUN npm run build

RUN npm install -g serve

# And finally the command to run the application
CMD ["serve", "-s", "-l", "5000", "build"]