# Base image
FROM node:20-alpine

# Working directory
WORKDIR /app

# Dependencies copy karo
COPY package.json package-lock.json ./
RUN npm install

# App code copy karo
COPY . .

# Build app
RUN npm run build

# Serve production build
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "3000"]

# Expose port
EXPOSE 3000
