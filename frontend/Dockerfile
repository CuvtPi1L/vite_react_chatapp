# Use an official Node.js runtime as a parent image
FROM node:21.7.1

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose port 3000 (the default port for Vite)
EXPOSE 5173

RUN npm run build
# Command to run the application
CMD ["npm", "run", "dev"]
