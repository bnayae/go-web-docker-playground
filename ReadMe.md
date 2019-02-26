# Dockerize

**docker build -t bnaya/calc-app:v1 . **

docker run -it --rm --name bnaya-calc -p 8080:80 -w /go/src/calc bnaya/calc-app:v1

for dev listening  
docker run -it --rm --name bnaya-calc -p 8080:80 -v c:/Users/Bnaya/go/src/github.com/bnayae/go-web-docker-playground/src:/go/volume/calc -w /go/volume/calc bnaya/calc-app:v1

- The docker run command is used to run a container from an image,
- The -it flag starts the container in an interactive mode,
- The --rm flag cleans out the container after it shuts down,
- The --name ma-instance names the container ma-instance,
- The -p 8080:8080 flag allows the container to be accessed at port 8080,
- The -v /app/MathApp:/go/src/MathApp is more involved.  
  It maps /app/MathApp from the machine to /go/src/MathApp in the container.  
  This makes -the development files available inside and outside the container, and
- The ma-image part specifies the image name to use in the container.
- The -w is the working directory
