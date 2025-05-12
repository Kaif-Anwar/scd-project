# Use Node.js 18 as the base image
FROM node:18

# Set working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies, forcing rebuild of native modules
RUN npm install --force

# Copy the rest of the backend code
COPY . .

# Expose the port your backend listens on (assumed 5000)
EXPOSE 5000

# Start the backend server
CMD ["node", "index.js"]