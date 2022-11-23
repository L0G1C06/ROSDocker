Crie a Dockerfile que está dentro dessa pasta

Depois digite o seguinte comando em um terminal dentro da pasta onde está a Dockerfile:

```sudo docker build -t roscore_c .```

Depois digite o outro comando no terminal dentro da pasta onde está a Dockerfile:

```sudo docker build -t rviz_c .```

Depois de realizar as builds, digite o seguinte comando:

```sudo docker run -it --rm --privileged --net=host roscore_c /bin/bash```

Vai abrir o terminal dentro do Docker

Insira o seguinte comando:

```roscore```

Abra um outro terminal e entre na pasta em que está a Dockerfile

Dentro desse segundo terminal digite o seguinte comando:

```xhost +local:docker```

E depois

```sudo docker run -it --rm --privileged --net=host --env=NVIDIA_VISIBLE_DEVICES=all --env=NVIDIA_DRIVER_CAPABILITIES=all --env=DISPLAY --env=QT_X11_NO_MITSHM=1 -v /tmp/.X11-unix:/tmp/.X11-unix rviz_c /bin/bash``` 

Vai abrir o terminal dentro do Docker

Insira o seguinte comando:

```rviz```

FIM
