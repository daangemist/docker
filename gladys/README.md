This will build a working [Gladys](https://github.com/GladysProject/Gladys) installation. The assumption is that there already
is a MySQL instance running on the docker host. The container will run on the host network,
there is no port mapping necessary because of this.

# Installation / setup

First, clone the Gladys repository into the subfolder git:

    git clone https://github.com/GladysProject/Gladys.git git
	
Then, build the image:

    git build --t matueranet/gladys-aarch64:latest .

# Run

Example command to run this (replace xxx with your MySQL password):

    docker run -d --restart always -e MYSQL_USER=gladys -e MYSQL_DATABASE=gladys -e MYSQL_PASSWORD=xxx --net="host" --name=gladys matueranet/gladys-aarch64:3.7.1
