# ${ROS2\\ 설치를\\ 위해\\ {\color{red}인터넷을\\ 연결해야\\ 합니다}}\ !!!!$
</br>

### 1. 터미널을 연다
![image](https://github.com/Jinsun-Lee/ros2_humble_install_sh/assets/68187536/ebae7005-9e85-4801-85e4-cd4da00bcc77)  



### 2. 아래 코드를 입력하고, 엔터를 누른다
```
curl -L -O https://github.com/Jinsun-Lee/ros2_humble_install_sh/raw/main/run.sh; sh run.sh
```
![image](https://github.com/Jinsun-Lee/ros2_humble_install_sh/assets/68187536/7d5688f6-3aa5-4fb4-9af4-712a0745dc06)



### 3. 비밀번호를 입력하고, 엔터를 누른다
![image](https://github.com/Jinsun-Lee/ros2_humble_install_sh/assets/68187536/4f54cb38-9201-4e63-8d7f-4991b5612ea3)



### (설치가 시작된다)
![image](https://github.com/Jinsun-Lee/ros2_humble_install_sh/assets/68187536/6df29532-e6f1-4df2-ab6b-1fcdb6b2d840)



### 4. 설치가 끝나면 확인한다
```
ROS가 제대로 설치된 경우에만 아래와 같은 출력이 나온다!

[INFO] [1716016137.177980873] [talker]: Publishing: 'Hello World: 1'
[INFO] [1716016138.177905936] [talker]: Publishing: 'Hello World: 2'
[INFO] [1716016139.177907257] [talker]: Publishing: 'Hello World: 3'
```
![image](https://github.com/Jinsun-Lee/ros2_humble_install_sh/assets/68187536/311336d4-d61b-4c72-beb8-4e65b7f496d5)






---
# 설치가 안 된 경우에만 아래 과정 진행!!! 
위와 같은 출력이 나오지 않는다면 제대로 설치되지 않은 것  
아래 명령어를 다시 실행하여 ROS를 설치하고 출력이 나오나 확인


### 설치
```sh
sh run.sh
```

### 설치 확인
```
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```
제대로 동작하지 않으면 설치 명령어를 한 번 더 실행해 볼 것



<details>
<summary>설치 제거</summary>
<div markdown="1">       

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
#sudo apt upgrade

source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```

</div>
</details>


