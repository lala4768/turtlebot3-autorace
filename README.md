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

<br>

## 주요 기능

1. **Wake Up Word**

   * "Hello Doovis" → 로봇이 대기 상태에서 활성화
   * openWakeWord 기반 커스텀 .tflite 모델 적용

2. **객체 인식**

   * YOLOv11 기반 공구 인식 (망치, 드라이버, 펜치, 렌치)
   * Roboflow 데이터셋 + 직접 촬영 데이터 병합 후 학습

3. **음성 명령 기반 제어**

   * "망치 오른쪽에 놔줘" → 객체 인식 + 좌표 변환 + Pick & Place 수행
   * "드라이버 가져와" / "가져가" → 신체 인식 + 공구 전달

4. **자연어 처리**

   * 접속사 기반 다중 명령 처리: "렌치 오른쪽에 두고 망치 가져와"
   * 간단한 일상 대화 대응

5. **안전 기능**

   * 운동 범위 제한, 특이점 배제
   * WebCam + RealSense 병행 사용으로 안전 확보
