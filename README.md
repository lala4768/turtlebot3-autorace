# Rokey 휴게소
디지털 트윈 기반 서비스 로봇 운영 시스템 구성

<br>

### Contributors
|정서윤|홍진규|나승원|이동기|
|----|----|----|----|
|**[???](https://github.com/)**|**[???](https://github.com/)**|**[lala4768](https://github.com/lala4768)**|**[???](https://github.com/)**|

<br>

## 프로젝트 개요

* **주제**
  
   휴게소 자율 주차 시스템 시뮬레이션
* **개발 배경**

  * 명절이나 연휴시 휴게소 주차에 어려움이 많음
  * 주차 공간이 협소할 경우 사고 위험이 높음
* **목표**

  * Lane Detection 및 Autorace 기술의 결합
  * 시뮬레이션 상에서 TurtleBot3의 자동주차 시스템 구현

<br>

# Flow Chart
`Default lane mode` → `traffic light`→`parking` → `Stop tunnel`
<img width="1084" height="464" alt="image" src="https://github.com/user-attachments/assets/4e189172-5c6c-4343-bded-6bf15d308db7" />

<br>

## 사용 기술 및 장비

* **언어 및 환경**: Python 3.10, Ubuntu 22.04, ROS2 Humble
* **도구**: Colab, VSCode
* **로봇 하드웨어**: X
* **로봇 소프트웨어**: Gazebo
