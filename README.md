<h1>How to install php 8.0 & Apache</h1>
<hr>
<h2>Commands to run Docker Container</h2>

1. build the Docker container:
```
docker build -t test-php
```

2. run the Docker container:
```
docker run -p 5000:80 -d -v $(pwd)/src:/var/www/html/ test-php
```

<h3>options:<h3>

1. flag -p: 5000 is the port of the local machine and 80 is the dafault port in Apache server.
2. flag -d: is the detached mode means that a Docker container runs in the background of your terminal
3. flah -v: works as a debugger mode, you can update the files and the container will be updated accordingly to the changes

<hr>
to change the php version, you only need to changed it in the docker file:

```
FROM php:7.2-apache
```
