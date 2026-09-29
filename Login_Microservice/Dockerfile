FROM node:24-alpine

WORKDIR /app

# Copy package requirements first for caching
COPY package*.json ./

RUN npm install

# Copy all source files
COPY . .

# Adjust port based on what index.js listens on (e.g., 3000 / 3001)
EXPOSE 5003

CMD ["node", "index.js"]