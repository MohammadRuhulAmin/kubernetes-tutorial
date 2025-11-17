# Use official Node.js image
FROM node:18

# Set working directory
WORKDIR /app

# Copy project files
COPY package*.json ./
COPY main.js ./

# Expose port
EXPOSE 3000

# Start the app
CMD ["node", "main.js"]
