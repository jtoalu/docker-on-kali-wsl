# Docker in Kali on WSL
I have been utilizing Kali on WSL for almost three years now (since Fall 2021). A challenge on https://dodcybersentinel.ctfd.io/ motivated me to learn how to run a Docker image in my Kali WSL. It turns out that it is easy to run a Docker image in Kali on WSL.
I searched the Internet and found https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-containers for the instructions of $${\color{lightgreen}Get \space started \space \space with \space Docker \space remote \space containers \space on \space WSL \space 2}$$
After downloading and installing the Docker Desktop for Windows from https://docs.docker.com/desktop/wsl/#download and configuring the necessary settings, a Docker image is ready to run in my Kali on WSL as shown by the following screenshot.

![alt text](https://github.com/jtoalu/docker-on-kali-wsl/blob/main/Screenshot%202024-05-22%20164653.png)

The rest of the steps is loading the Docker file through the Kali on WSL terminal with the following commands:
docker load -i {filename}.tar
docker images
docker run -d -p 1234:80 {image_id}
docker ps
Replace {filename}.tar with the actual filename and {image_id} with the appropriate image ID from the docker images output.

Please see the following screenshot for more information.

![alt text](https://github.com/jtoalu/docker-on-kali-wsl/blob/main/Screenshot%202024-05-22%20170554.png)

A website which was saved into a Docker instance can now be seen on my laptop by accessing http://localhost:1234/ as shown by the following screenshot.

![alt text](https://github.com/jtoalu/docker-on-kali-wsl/blob/main/Screenshot%202024-05-22%20171821.png)

Note for Self: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax and https://stackoverflow.com/questions/11509830/how-to-add-color-to-githubs-readme-md-file 
