FROM node:22-alpine

# Instalar pnpm
RUN corepack enable && corepack prepare pnpm@latest --activate

WORKDIR /app

# Instalar dependencias de desarrollo necesarias
RUN apk add --no-cache libc6-compat

# Los archivos se montarán como volumen
CMD ["pnpm", "dev"]
