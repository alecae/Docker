# Base image
FROM node:14.17.5-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files to the working directory
COPY . .

# Build the production version of the application
RUN npm run build

# Expose the port used by the application
EXPOSE 3000

# Start the application
CMD ["npm", "start"]
