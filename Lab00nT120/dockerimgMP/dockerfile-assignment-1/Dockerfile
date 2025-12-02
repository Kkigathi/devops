# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.
# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.

# --- INSTALL DEPENDENCIES HERE ---
FROM node:6-alpine
EXPOSE 3000
RUN apk add --update tini
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# 1. Copy only the package.json file first
COPY package.json package.json

# 2. <<< ADD THIS CRITICAL STEP! >>>
# Install dependencies based on package.json
RUN npm install && npm cache clean

# 3. Copy all other source files
COPY . .

# 4. Execute the application
CMD ["tini", "--", "node", "./bin/www"]