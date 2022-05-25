# Movi
![https://lab.ssafy.com/s06-iot-control-sub2/S06P22A501/uploads/b71a9d785a2a244fe3cf7cde84f9aca3/Logo.png](https://lab.ssafy.com/s06-iot-control-sub2/S06P22A501/uploads/b71a9d785a2a244fe3cf7cde84f9aca3/Logo.png)
- SSAFY 6기 특화프로젝트 A501 
- 인공지능과 자율주행을 접목한 화물 운송 로봇 Movi 입니다. 


# 팀 소개

김남훈: 팀장, 인지 파트, Git

이규은: 인지 파트, 발표   

박홍규: 인지 파트, Jira 

이진행: 판단/제어 파트, 시뮬레이터 환경 구성, Notion 

이진희: 판단/제어 파트, UCC  

전건하: Web(Full-Stack), 배포   

# 개요

1. 개발 기간 : 2022년 2월 21일 - 2022년 4월 8일 (7주)
2. 목표 
    - 화물 창고 내에서 택배를 인식하고, 목표 위치로 운송하는 로봇을 구현합니다.
    - 택배에 부착된 QR코드를 인식하고, 이를 토대로 목표 위치를 설정합니다.
    - 라이다센서를 통해 맵을 생성, 이를 이용하여 경로 생성을 합니다.
3. 기대효과
    
    [뉴스 : '택배법 통과됐는데...' 택배기사들이 '총파업' 준비하는 이유](https://www.vop.co.kr/A00001540619.html)
    
    - 배송을 위한 선별 분류 및 상차는 택배 기사의 업무로,   
    택배가 많아질수록 기사의 업무가 과중된다는 문제점이 있었습니다.
    - 또한, 택배의 오분류로 발생한 작업의 비용은   
    택배 기사 수수료에서 차감하는 문제점이 있었습니다.
    
    ⇒  물류 대란과 같은 상황에서도 안정적으로 택배를 분류 할 수 있을것으로 기대됩니다.   
    또한, 24/7 근무가 가능하므로, 업무의 효율성이 증대될 것으로 예상합니다.
    
    ⇒  이러한 오분류 문제를 Movi를 통해 낮추어,   
    택배기사의 업무 부담을 줄 일 수 있을것으로 예상합니다
    
4. 기획내용   
    [기획 발표 pdf](../Movi/Document/smart_iot_movi.pdf)
  
5. 프로젝트 UCC   
    [Movi UCC](https://youtu.be/5xxZX21mxcA)
    

# 프로젝트 소개

- 2022년 초 다양한 요인으로 인하여 택배 물류 대란이 발생하였습니다.
- 택배 기사들이 직접 담당 구역의 택배를 분류하고, 적재하는 업무까지 담당하여 택배 기사들의 업무가 과중되었습니다.
- 이를 해결하기 위해, 택배를 자동으로 분류해주고, 적재해주는 로봇이 있으면 좋겠다는 생각이 들었습니다.
- IoT, Ai, 자율주행을 이용하여 화물 창고 내 택배 자동 분류 로봇을 구현하고자 하였습니다.

# 주요 기능

### 맵 생성

- 2D 라이다 센서를 이용해 맵을 생성하고, 이를 경로탐색에 활용합니다.
        ![mapping](https://user-images.githubusercontent.com/70011316/170166584-a5078c75-c129-4e24-b158-50ec206703e0.gif)

### 택배 운송

1. 박스 탐색
    - 화물 창고 내 저장위치에 저장된 상자를 탐색합니다.
        
        ![box_recog](https://user-images.githubusercontent.com/70011316/170166590-4a3c6555-7b90-4f30-b4ed-e90555120707.gif)
        
2. 박스 QR코드 인식
    - 상자를 인식했다면, 상자에 접근하면서 상자에 부착된 QR코드를 확인합니다.
        
        ![qr_recog](https://user-images.githubusercontent.com/70011316/170166586-3658777b-573d-4afe-b903-e8da77cf1bb9.gif)
        
3. 박스 운송
    - 인식한 qr코드의 정보를 이용하여, 운송 위치로 물건을 배달합니다.
        
        ![box_up](https://user-images.githubusercontent.com/70011316/170166591-8fe00a49-e401-4e77-98d2-f35306ca63df.gif)
        ![box_down](https://user-images.githubusercontent.com/70011316/170166589-a4edb94f-8fc7-4426-ae4c-0206eee1fa24.gif)

        

# 서비스 아키텍쳐

![architecture](https://user-images.githubusercontent.com/70011316/170166791-42b5dde9-025c-47fb-ad2e-9fe513c58678.png)


### WEB

- Frontend : Vue.js 3, Element Plus, vite
- Backend : Django, Python-socketio
- DB : sqlite3
- AI : tensorflow

### 로봇

- ROS2 Eloquent, OpenCV, TensorFlow
- SSAFY 제공 Unity 기반 시뮬레이터

### 협업 툴

- Git, JIRA

# 기술 상세

[Movi 기술 상세 설명](https://www.notion.so/Movi-28af65a9c6cc4c04b10a7f45b7a28cc7)

# ETC

[고도화 방안](https://www.notion.so/b47e09fa977146c2a619620c54b7817e)

[프로젝트 실행법](https://www.notion.so/a4e1486e17444b558d5a56b85756e4d6)