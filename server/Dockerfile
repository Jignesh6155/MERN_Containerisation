# Step 1: Use an official Node.js image as the base image
FROM node:16

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json to the container
COPY server/package*.json ./

# Step 4: Install the server dependencies
RUN npm install

# Step 5: Copy the rest of the server code to the container
COPY server/ .

# Step 6: Expose port 8080 (default backend port)
EXPOSE 8080

# Step 7: Command to run the Node.js server
CMD ["npm", "start"]