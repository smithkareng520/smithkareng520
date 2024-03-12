>安装 **yum-utils** 并添加源
>为了安装Docker，我们需要首先安装**yum-utils**，以便添加Docker的源
  
1.`yum install -y yum-utils`  

2.`yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo  `

>安装Docker
>直接使用yum命令即可安装Docker。

```yum install docker-ce docker-ce-cli containerd.io```
>运行并设置**自启动**

>Docker安装完成后不会自动运行，需要手动运行：

```systemctl start docker```
>为了让 Docker 在每次重启系统的时候能够自动运行，还需要设置自启动：

```systemctl enable docker```
>至此就大功告成。可以使用hello-world镜像验证一下：

```docker run hello-world```

看到以下输出即为成功：  

```Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
93288797bd35: Pull complete
Digest: sha256:37a0b92b08d4919615c3ee023f7ddb068d12b8387475d64c622ac30f45c29c51
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/```


