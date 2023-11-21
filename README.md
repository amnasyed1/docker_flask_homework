# docker_flask_homework

## Part 1: Dockerizing a Single Flask Application
1. In Google Cloud Shell, create a folder named `Part1`
2. Create a `Dockerfile`, `app.py` file, and a `requirements.txt` file within the folder.
3. In the terminal, type `docker build -t <the name of the image you would like to build> . `
4. To see the images that it created type `docker images` into the terminal. It then shows information about the image that you just created, the repository name, tag, image ID, when it was created and the size.
5. Next, to run the image `docker run -p <newport:oldport> <name of image>`
   - "-p" is the port; if you would like to run the image on a port different from the one you exposed in the Dockerfile and documented in the app.py, then write the new port, then a colon`:` and then the old port. For example (-p 8005:5000)
6. To preview the image, click `Web Preview`, `Change Port`, enter the new port number, for instance, utilizing the example above, type `8005` and then click `Change and Preview`, and your image will be run in a container and can be viewed without any issues.
  - If you refresh the page running the image, in youe terminal you will be able to see `GET responses` and dockerized
7. To detach `docker run -d -p 8005:5000 <name of image>` and this will give you an ID. 
8. Type `docker ps` to see the information in a list/table structure with contents such as the container ID, image name, command, when it was created, the status, ports its exposed on etc.
9. To stop the container from running type `docker stop <container ID>`
10. To double check nothing is running, type `docker ps`, and no list should be seen under the table.

## Part 2: Multi-Container Setup with Docker Compose 
