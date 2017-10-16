FROM node:boron

# Create src folder
RUN mkdir /src

WORKDIR /src
ADD ./git /src

ENV NODE_ENV production
RUN npm install && npm install -g grunt-cli && grunt buildProd

# Export listening port
EXPOSE 8080

CMD ["node" ,"app.js"]

