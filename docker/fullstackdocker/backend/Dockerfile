# use official node image
FROM node:22-alpine
# set working directory
WORKDIR /app
# copy package.json and package-lock.json files inside the container's working directory
COPY package*.json ./
# install dependencies
RUN npm install
# copy the rest of the application code inside the container's working directory
COPY . .
# expose the port the application runs on
EXPOSE 5000
# run the application
CMD ["npm", "start"]