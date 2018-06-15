This is a React app bootstrapped with creat-react-app with configuration to build it into a Docker image

## To build Docker image of this app

- `docker image build -t react:app .` (You can replace 'react:app' to whatever you want, e.g.: 'myreact:16')
- To see the image, run `docker image ls react:app`

## To run the Docker container

- `docker container run -it -p 3000:3000 react:app`
- Open the browser and go to 'http://localhost:3000' to see the app

## To run the Docker container and see the output from hot-reloading in your terminal

- `docker container run -it -p 3000:3000 -p 35729:35729 -v $(pwd):/app react:app`

## To run the Docker container and build the app

- `docker container run -it -v $(pwd):/app react:app build`

## To run the Docker container and run test for the app

- `docker container run -it -v $(pwd):/app react:app test`

## You can just get the Docker image that I built from Docker hub

- Simply run `docker pull shiang/react`

## Special thanks to

[this guide](https://www.peterbe.com/plog/how-to-create-react-app-with-docker)
