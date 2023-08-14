FROM mongo:latest

EXPOSE 27017

# Create a directory for MongoDB data
RUN mkdir -p /data/db

# Set the working directory
WORKDIR /data/db

# Start the MongoDB server
CMD ["mongod"]