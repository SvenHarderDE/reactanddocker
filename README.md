## Start docker development server
docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image-id>
docker-compose up

## Testing
docker run -it <image-id> npm run test

### Live Testing (run test in existing container)
docker exec -it <image-id> npm run test
docker-compose up (no -it)

## run live Server
docker build .
docker run -p 8080:80 <image-id>