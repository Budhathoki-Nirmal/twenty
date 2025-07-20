FROM node:18-alpine

WORKDIR /app

# Copy only the server and shared code
COPY packages/twenty-server ./packages/twenty-server
COPY packages/twenty-shared ./packages/twenty-shared
COPY package.json yarn.lock ./

# Install only what's needed
WORKDIR /app/packages/twenty-server
RUN yarn install --production

# Expose and start
EXPOSE 3000
CMD ["node", "src/main.js"]
