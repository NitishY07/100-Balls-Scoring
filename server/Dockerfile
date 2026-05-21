FROM node:20-slim

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy application files
COPY . .

# Create uploads and matches directories for persistence
RUN mkdir -p uploads matches

# Expose port (Fly.io typically routes to port 8080 or respects the PORT env var)
ENV PORT=5000
EXPOSE 5000

# Start the server
CMD ["node", "server.js"]
