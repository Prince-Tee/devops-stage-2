
FROM node:16

WORKDIR /app

COPY . /app

RUN npm install

RUN npm run build

# Make port 3000 available
EXPOSE 3000

# Run the app
CMD ["npx", "serve", "-s", "build"]
