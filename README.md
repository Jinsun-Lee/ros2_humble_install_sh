# 다운로드 + 설치
```
curl -L -O https://github.com/Jinsun-Lee/ros2_humble_install_sh/blob/main/run.sh; sh run.sh
```

# 설치 확인
```
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```

# 설치
```sh
sh run.sh
```

# 삭제
```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock*
sudo dpkg --configure -a
sudo apt update
sudo apt remove ~nros-humble-* && sudo apt autoremove
sudo rm /etc/apt/sources.list.d/ros2.list
sudo apt update
sudo apt autoremove
sudo apt upgrade

source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```
