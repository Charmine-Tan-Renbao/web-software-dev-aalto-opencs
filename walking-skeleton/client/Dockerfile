FROM denoland/deno:alpine-2.1.9

WORKDIR /app

COPY package.json ./

RUN deno install

COPY . .

WORKDIR /app

CMD ["run", "-A", "--node-modules-dir", "npm:vite", "dev", "--host", "0.0.0.0", "--port", "5173"]