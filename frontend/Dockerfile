# frontend/Dockerfile
# Step 1: Build the React app
FROM node:14 AS build

WORKDIR /app

# Install dependencies
COPY package.json /app/
COPY package-lock.json /app/
RUN npm install

# Copy all files
COPY . /app/

# Build the app
RUN npm run build

# Step 2: Serve the React app
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
