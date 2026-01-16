# Docker-documentation

### Verify installation:
```docker --version```
```docker compose version```


## Dockerfile:


```FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
```

## Building the Image:

```docker build -t <app-name> .```


##  Running the Application:

```docker run -p 3000:3000 <app-name>```


##  Enter a running container:

```docker exec -it container_name sh```

## Pulling Images:

```docker pull nginx```


## Pull a specific tag:
```docker pull node:18-alpine```

## List local images:

```docker images```

## agging Images:

```docker push <username>/<app-name>:1.0.0```

## Running Containers:

```docker run <app-name>```

## Run with environment variables:

```docker run -e NODE_ENV=production <app-name>```

## Stopping Container:

```docker stop <container_id>```

## Remove a container:

```docker rm container_id```

## Removing Images:

```docker rmi <image_id>```