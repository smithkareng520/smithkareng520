>安装 **yum-utils** 并添加源
>为了安装Docker，我们需要首先安装**yum-utils**，以便添加Docker的源
  
1.`yum install -y yum-utils`  

2.`yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo  `

>安装Docker
>直接使用yum命令即可安装Docker。

`yum install docker-ce docker-ce-cli containerd.io`
>运行并设置**自启动**

>Docker安装完成后不会自动运行，需要手动运行：

`systemctl start docker`
>为了让 Docker 在每次重启系统的时候能够自动运行，还需要设置自启动：

`systemctl enable docker`
>至此就大功告成。可以使用hello-world镜像验证一下：

`docker run hello-world`
