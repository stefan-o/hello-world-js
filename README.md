## Node.js - Hello World Example with Docker

Just a simple example of displaying "Hello World!" with express and Docker.

Running without Docker:
```
$ git clone git@github.com:stefan-o/hello-world-js.git hello-world-js
$ cd hello-world-js
$ npm install
$ npm start
$ curl http://localhost:3000
# It will return:
Hello World!
```

Running with Docker:
```
$ git clone git@github.com:stefan-o/hello-world-js.git hello-world-js
$ cd hello-world-js
$ docker build -t hello-world-js .
$ docker run -d -p 3000:3000 --name hello-world-js hello-world-js
$ curl http://DOCKER_HOST:3000
# It will return:
Hello World!
```

To kill the running container:
```
$ docker kill hello-world-js
```

Remove the container:
```
$ docker rm hello-world-js
```
