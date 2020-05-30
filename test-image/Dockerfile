FROM node:6-alpine

# Create feports directory
RUN mkdir -p /jUnit

# Create a server directory
RUN mkdir -p /home/node/tests
WORKDIR /home/node/tests

# Install app dependencies
COPY /test-image/package.json /home/node/tests
RUN npm install

# Copy test source
COPY app.js /home/node/tests

EXPOSE 9000

CMD [ "npm", "test" ]
