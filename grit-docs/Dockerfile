FROM node:lts@sha256:8530f76a96d88820d288761f022e318970dda93d01536919fbc16076b7983e63

WORKDIR /app

RUN npm install -g pnpm@10.30.1

COPY package.json /app/package.json
COPY pnpm-lock.yaml /app/pnpm-lock.yaml

RUN pnpm install --frozen-lockfile

COPY . .

EXPOSE 4242

CMD ["pnpm", "start:docker"]
