# 다운로드 + 설치
```
curl -L -O https://github.com/Jinsun-Lee/ros2_humble_install_sh/raw/main/run.sh; sh run.sh
```
run.sh 파일이 없을 경우 터미널에서 위의 명령어만 실행하면 파일 다운로드하고 설치 진행함  
</br></br>


# 설치
```sh
sh run.sh
```
git clone이나 코드를 복사해서 파일이 있을 경우   
run.sh 파일이 있는 경로에서 위의 명령어 실행
</br></br>



# 설치 확인
```
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```
제대로 동작하지 않으면 설치 명령어를 한 번 더 실행해 볼 것
</br></br>



# 설치 제거
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
신중히 사용할 것
