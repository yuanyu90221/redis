# The setup for the redis server
docker pull redis:3.2

# Run the docker command to start redis server
docker run -p 6379:6379 -v $PWD/data:/data  -d redis:3.2 redis-server --appendonly yes

# Check docker status
docker ps

# Connect to Container redis
docker run -it redis:3.2 redis-cli -h ${host}