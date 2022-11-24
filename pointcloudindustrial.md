# script para rodar uma nuvem de pontos de uma sala industrial

### clone na pasta home
```git clone https://github.com/ros-industrial/industrial_training```

### entrando na pasta onde está a nuvem de pontos
```cd /root/industrial_training/exercises/4.2```

### instalando as dependencias no Docker
```sudo apt install ros-melodic-pcl-ros```

```sudo apt install pcl-tools```

### dando um rosrun para gerar a nuvem de pontos
```rosrun pcl_ros pcd_to_pointcloud table.pcd 0.1 _frame_id:=map cloud_pcd:=orig_cloud_pcd```

### rodar o rviz
```rosrun rviz rviz```

### adicionar o tópico PointCloud2 na árvore de tópicos
  1. Selecione Add
  2. Selecione PointCloud2
  3. Expanda PointCloud2 na árvore de tópicos e selecione um tópico do drop down topic
    . Dica: se está usando a point cloud clonada, o tópico desejado ser
