# script para rodar uma nuvem de pontos de uma sala industrial

### clone na pasta home
```git clone https://github.com/ros-industrial/industrial_training```

```cd /root/industrial_training/exercises/4.2```

```sudo apt install ros-melodic-pcl-ros```

```sudo apt install pcl-tools```

```rosrun pcl_ros pcd_to_pointcloud table.pcd 0.1 _frame_id:=map cloud_pcd:=orig_cloud_pcd```
