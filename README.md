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
11. To remove the container type `docker rm <container ID>`
12. Lastly, to clean and remove everything (system prune) `docker system prune -a -f` .
    
## Part 2: Multi-Container Setup with Docker Compose 
1. Create a folder named `Part2`.
2. Create a Docker Compose file `docker-compose.yml`, within the folder.
3. In additon, within the Part2 folder, create a folder named `flask1` and populate the folder with a `Dockerfile`, `app.py` file, and `requirements.txt` file. Also, create a `templates` folder in order to create a flask app.
4. Next create a `flask2` folder also within the `Part2` folder. Follow the same steps you did for creating the flask1 folder.
5. Ensure the code works by `python app.py` for each flask app.
6. In the terminal, ensure you are in the write folder/folders, and type `docker-compose build` to build the images within the flask apps.
7. After that, to run the images in the containers, type `docker-compose up`.
8. Similar to the  steps in Part 1, to preview the images, click `Web Preview`, `Change Port`, enter the new port number, for instance, utilizing the flask1 as an example (in the docker-compose.yml file it states which flask app utilizes which ports),type `5001` to preview flask1 and then click `Change and Preview`, and your image will be run in a container and can be viewed without any issues.
9. Next, to show a list of the containers as in Part1, in the terminal type `docker-compose ps`.
10. To stop the containers, type `docker-compose down`.
11. To remove a container, `docker rm <container ID>`.
12. Finally, to clean and remove everything (system prune) `docker system prune -a -f` .

## Role of Docker Compose, How It Differs from Using Docker Alone, and Reflection 
Docker Compose allows for running and managing multi-container docker applications, as we can see in Part 2. When using Docker alone, containers are ran and managed individually. Docker Compose can be best utilized when working on a multi-container or complex apps to reduce time and imporve productivity. The process of using and working with Docker was seamless and easy. The most important thing when working on especially Part2 with multi-containers is organization. Once, your workspace is organized with the right files in the right folders and the right folders in their respective bigger folders, it makes the process of utilizing Docker easy and enjoyable. 
