# Step 1: Set the base image
FROM node:16 AS build

# Step 2: Set the working directory
WORKDIR /app

# Step 3: Copy package.json and package-lock.json (if any)
COPY client/package*.json ./

# Step 4: Install npm version compatible with node 16
RUN npm install -g npm@8.19.4

# Step 5: Install dependencies (with legacy-peer-deps to avoid conflicts)
RUN npm install --legacy-peer-deps

# Step 6: Copy the rest of the application code
COPY client/ .

# Step 7: Build the app (if needed)
RUN npm run build

# Step 8: Expose the port and run the app (adjust as needed)
EXPOSE 3000
CMD ["npm", "start"]

#docker build -f client/Dockerfile -t client-image:latest .
#for tomorrow focus on downloading the updated npm 
#check facebookloogin react version its outdated so job is to make a version that can work with current npm