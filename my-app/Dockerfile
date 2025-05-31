# Dockerfile (inside my-app/)
FROM node:20

WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy all source files
COPY . .

# Build the app
RUN npm run build

EXPOSE 3000
# CMD ["npm", "start"]
CMD ["npm", "run", "dev"]
