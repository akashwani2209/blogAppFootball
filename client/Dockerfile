# Use a base image with Node.js
FROM node:18

# Set the working directory
WORKDIR /app/client

# Copy package.json and yarn.lock to the container
COPY package.json yarn.lock ./

# Install dependencies using Yarn
RUN yarn install

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Build the client application
RUN npm run build

# Build the client application using Yarn
RUN yarn build

# Expose the port the app runs on
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]
