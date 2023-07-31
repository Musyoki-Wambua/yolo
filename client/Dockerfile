# Use an appropriate base image
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package.json package.json

# Install project dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .                                                                                                                                                                                                                                    

# Expose the port on which the client application will run (if applicable)
EXPOSE 3000

# Specify the command to start the client application
CMD ["npm", "start"]
