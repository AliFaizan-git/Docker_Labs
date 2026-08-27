FROM node:20-alpine

WORKDIR /myapp

COPY package*.json ./

RUN npm ci

COPY . .

# Expose Vite's default dev port
EXPOSE 5173

# Run the dev server and bind to 0.0.0.0 so host machine can access it
CMD ["npm", "run", "dev", "--", "--host"]