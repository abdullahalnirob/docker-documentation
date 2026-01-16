# Docker-documentation

### Verify installation:
```bash
docker --version
```

```bash
docker compose version
```


## Dockerfile:


```bash
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
```

## Building the Image:

```bash
docker build -t <app-name> .
```


##  Running the Application:

```bash
docker run -p 3000:3000 <app-name>
```


##  Enter a running container:

```bash
docker exec -it container_name sh
```

## Pulling Images:

```bash
docker pull nginx
```


## Pull a specific tag:
```bash
docker pull node:18-alpine
```

## List local images:

```bash
docker images
```

## agging Images:

```bash
docker push <username>/<app-name>:1.0.0
```

## Running Containers:

```bash
docker run <app-name>
```

## Run with environment variables:

```bash
docker run -e NODE_ENV=production <app-name>
```

## Stopping Container:

```bash
docker stop <container_id>
```

## Remove a container:

```bash 
docker rm container_id
```

## Removing Images:

```bash
docker rmi <image_id>
```