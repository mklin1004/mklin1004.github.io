Docker for windows to install Linux

**Installing the required software with Docker**

1.  download docker for desktop
    (<https://www.docker.com/products/docker-desktop>)

2.  you will need to set up account with docker.com. After you logged
    in, select docker desktop for windows.

3.  download and install. Just hit "next" till the end.

4.  you will be informed to restart your computer.

5.  After restart, enable your powershell and type "docker -v" to see if
    PATH has been setup correctly and docker can work correctly. You
    will see your docker version with this command, and that means it
    worked.

6.  The default docker is Linux container, and you have it now. If you
    need to switch, use the docker whale at status bar.

    ![](media/image1.png){width="6.25in" height="4.479166666666667in"}

7.  You can click Kitematic and download, extract it to C:\\Program
    Files\\Docker\\Kitematic, to get a graphic interface for Docker.

8.  open powershell and run

    **docker build -t bio
    https://raw.githubusercontent.com/PacktPublishing/Bioinformatics-with-Python-Cookbook-Second-Edition/master/docker/Dockerfile**

    to setup the python (anaconda) environment for the book. It may take
    a long time (over 30 minutes) to install, depending on your hardware
    structure.

9.  **run "docker run -ti -p 9875:9875 -v YOUR\_DIRECTORY:/data bio".**
    You need to create a folder to share with docker. Your windows 10
    username need to have a password for docker to login. You will see a
    token on powershell like
    <http://ff33742f0583:9875/?token=6badd00c5199e9a48cf7a558bbe7331f8f17460f8ea6f1f4>

> **go to chrome and type localhost:**9875

copy this token and enter it in the jupyter notebook page to use the
jupyter notebook for the book.

> I use "**docker run -ti -p 9875:9875 -v c:\\biopython:/data bio"**
>
> ![](media/image2.png){width="4.888888888888889in" height="2.75in"}

10.
