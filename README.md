#  [빅데이터 청년인재 BIG X CAMPUS 프로젝트]
#### 프로젝트명: 영상 등급 분류 보조 시스템(Picker) 
#### 팀명: .999 (9할 9푼 9리)
--- 

### 1. 목적
  DDDM(Data Driven Decision Making)을 통해 객관적으로 영화 등급을 분류할 수 있게 할것  
  자동화 시스템을 통해 영상 컨텐츠 증가에 따른 심사 인력 부족 현상을 해결할 것

### 2. 주요 기능
  영상 내 유해 요소 감지  
  영상 내 유해 요소 타임라인, 비중 정보 제공

### 3. 진행 과정
#### 3-1. 데이터 수집 및 전처리
##### (1) 데이터 수집
  영상 등급 위원회에서 고려하는 7가지 요소(주제 대사, 공포, 약물, 선정성, 폭력성, 모방위험) 중 `선정성` `폭력성` `모방위험`에 초점을 맞춤
  ![dataset](https://github.com/krispedia/.999/blob/master/_ect/dataset.jpg)  

##### (2) 데이터 전처리
  전처리 도구 : [VIA](http://www.robots.ox.ac.uk/~vgg/software/via/)
  ![annotation](https://github.com/krispedia/.999/blob/master/_ect/annotation.jpg)
  <전처리 기준>
  - 담배<br>
    `담배를 입에 물고 있는 경우`
    - 코 아래부터 입 포함 아래턱 까지
    - 양 볼의 절반 포함
    `담배를 손에 들고 있는 경우`
    - 손가락과 손 포함 손목까지
    `담배를 손에 들고 입으로 물고 있는 경우`
    - 손가락 포함 양볼 절반, 코 아래부터 입포함 아래턱까지
  - 총<br>

  - 칼<br>
    `칼 형태가 드러나있을 경우`
    - 칼 윤곽선만 마스킹
    `사람이 칼을 쥐고있어 칼에서 칼날만 드러날 경우`
    - 칼날과 손(주먹)까지 마스킹
  - 가슴<br>
    `뚜렷한 선이 없는 경우`
    - 정확한 가슴 모양이 아닌 조금 폭 넓게 마스킹 함
    `가슴의 일부가 가려진 경우`
    - 손과 같은 다른 것이 일부만 가리는 경우에는 같이 포함하여 마스킹함
    `가슴의 반 이상이 가려진 경우`
    - 옷이나, 손 등으로 가슴의 반 이상이 가려진 경우에는 그것들을 제외하고 마스킹함  
  - 주류<br>
#### 3-2. 모델 학습
##### (1) 모델 선정
##### (2) 모델 학습 방법
##### (3) 모델 최적화
  ![hyperparameter](https://github.com/krispedia/.999/blob/master/_ect/hyperparameter.jpg)
#### 3-3. 웹사이트 구현
  ![service](https://github.com/krispedia/.999/blob/master/_ect/service.jpg)
### 4. 결과물
  ![result](https://github.com/krispedia/.999/blob/master/_ect/website.jpg)


