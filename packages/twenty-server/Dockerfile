# Use official Node LTS image
FROM node:22-slim

# Enable corepack for Yarn
RUN npm i -g corepack && corepack enable

# Set working directory inside the container
WORKDIR /app

# Copy only relevant monorepo files
COPY . .

# Focus install only for twenty-server
RUN yarn workspaces focus twenty-server --production

# Build the app
RUN yarn build

# Expose port (change if your app uses a different port)
EXPOSE 3000

# Start the app
CMD ["yarn", "start"]
