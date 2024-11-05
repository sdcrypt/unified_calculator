# frontend/Dockerfile

# Use an official Node.js image
FROM node:14-alpine

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json .
RUN npm install

# Copy the React project files
COPY . .

# Expose port (default React app port is 3000)
EXPOSE 3000

# Start the React app
CMD ["npm", "start"]