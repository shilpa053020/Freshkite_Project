# ---------- Base Stage ----------
    FROM node:18-alpine AS base
    WORKDIR /app
    COPY package.json package-lock.json ./
    RUN npm install
    
    # ---------- Dev Stage ----------
    FROM base AS dev
    WORKDIR /app
    COPY . .
    
    EXPOSE 3000
    CMD ["npm", "run", "dev"]
    