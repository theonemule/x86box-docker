# 86BOX IN A CONTAINER PLAYABLE THROUGH A BROWSER

Now, you can run DOS, Windows 95, Windows 98, Windows 98 SE, and Windows XP in a container!

[<img src="retroarch.jpg" width="50%">](https://www.youtube.com/watch?v=6gqXNirjNeU "RETRTOARCH IN A CONTAINER")

RetroArch in a container typically requires that you have some kind of specialized client to play the games over the network. Not anymore. This implementation uses a web browser as the client without the need for anything else installed on your client.

The implementation is pretty straightforward. You can run it locally, or run it on a cloud-hosted service, like Azure Container Instances or Azure Kubernetes Services. In any case, you'll probably want to allocate at least 2 Gigs of RAM and 2 CPUs to make things run smoothly -- more for more graphic-intense emulators.

If you want to build it, simply clone the repo and run Docker Build.

`docker build -t 86box . ` 

Alternately, you can pull the image from Docker Hub.

`docker pull blaize/86box`

To run this locally, run a Docker command:

`docker run -v /path/to/your/isos:/isos -p 80:80 blaize/86box`

Once the container is running, point your browser to the IP address or host name of your Docker environment. Retroarch has a basic install here.

Build your oldschool PC and run your favorite OSs in the cloud!
