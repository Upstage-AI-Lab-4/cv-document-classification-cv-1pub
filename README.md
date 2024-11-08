# Document Type Classification - Competition 
- 문서는 금융, 보험, 물류, 의료 등 도메인을 가리지 않고 많이 취급됩니다. 이 대회는 다양한 종류의 문서 이미지의 클래스를 예측합니다.
<br>

## 프로젝트 소개
- 이번 대회는 computer vision domain에서 가장 중요한 태스크인 이미지 분류 대회입니다.
- 이미지 분류란 주어진 이미지를 여러 클래스 중 하나로 분류하는 작업입니다. 이러한 이미지 분류는 의료, 패션, 보안 등 여러 현업에서 기초적으로 활용되는 태스크입니다. 딥러닝과 컴퓨터 비전 기술의 발전으로 인한 뛰어난 성능을 통해 현업에서 많은 가치를 창출하고 있습니다.

![image](https://github.com/user-attachments/assets/a283599d-e341-4e64-abf2-86725543004d)

- 그 중, 이번 대회는 문서 타입 분류를 위한 이미지 분류 대회입니다. 문서 데이터는 금융, 의료, 보험, 물류 등 산업 전반에 가장 많은 데이터이며, 많은 대기업에서 디지털 혁신을 위해 문서 유형을 분류하고자 합니다. 이러한 문서 타입 분류는 의료, 금융 등 여러 비즈니스 분야에서 대량의 문서 이미지를 식별하고 자동화 처리를 가능케 할 수 있습니다.

<br>

## 팀원 구성

<div align="center">

| **팀장** | **팀원 1** | **팀원 2** | **팀원 3** | **팀원 4** |
| :------: |  :------: | :------: | :------: | :------: |
|[<img src="https://avatars.githubusercontent.com/u/97029997?v=4" height=150 width=150><br/>이동호](https://github.com/Horidong)|[<img src="https://avatars.githubusercontent.com/u/74906042?v=4" height=150 width=150> <br/> 김이준](https://github.com/yijoon009) |[<img src="https://avatars.githubusercontent.com/u/177802089?v=4" height=150 width=150> <br/> 마서연](https://github.com/sma002452) |[<img src="https://avatars.githubusercontent.com/u/40532035?v=4" height=150 width=150> <br/> 박주연](https://github.com/pbcs0321) |[<img src="https://avatars.githubusercontent.com/u/40630127?v=4" height=150 width=150> <br/> 주남정](https://github.com/namjeong-joo) |
</div>

<br>

## 1. 개발 환경

- 주 언어 : Python 3.10
- 개발환경 : Upstage AI Stage Server
- MLOps : WandB

<br>

## 2. 채택한 개발 기술과 전략

### WandB
- Model 별로 Training 중 Epoch과 Folk에 따른 Loss값과 F1 Score 분석에 사용
- 해당 F1 Score에 따라 가장 성능 좋은 모델을 최종 예측에 사용
![image](https://github.com/user-attachments/assets/3cd02da1-38f3-417a-91e0-ac4fb40512e5)

### 데이터 증강
**- Augraphy**
  - 문서 데이터 변형 등의 증강에 유리

![image](https://github.com/user-attachments/assets/8003eb82-7d4c-4fa7-ac95-f17a97b5fdac)

**- Albumentation**
  - 이미지의 여러가지 왜곡, 변형 등의 증강에 유리

![image](https://github.com/user-attachments/assets/0c3d215f-2697-47a5-9a11-f4fc2bbd01c6)

<br>

## 3. 프로젝트 구조
```
├── README.md
├── .gitignore
├── data                                     # Training and Test Dataset
├── output
     ├── models                              # Model Archive
     └── output                              # Prediction Output Archive
└── code
     ├── data_augment.ipynb                  # Data Augmentation and Write
     ├── model_training.ipynb                # Model Training and Export
     └── model_load_and_prediction.ipynb     # Model Load from '../output/models' and Prediction
```

<br>

## 4. 개발 기간 및 특징

### 개발 기간
- 전체 개발 기간 : 2024-10-29 ~ 2024-11-08
- 기능 구현 : 2024-10-29 ~ 2024-11-08
<br>

### 데이터 증강 내용
- 기본 1570개의 학습 데이터를 증강
- Augraphy의 DirtyDrum 및 NoiseTexture를 이용
- Albumentations의 Flip, Rotate, BrightContrast, Defocus, Gamma, HueSaturation, MedianBlur, MotionBlur, GaussNoise 등을 이용
- 최종 9만5천여개의 학습 데이터를 사용

![image](https://github.com/user-attachments/assets/b2687c83-c3bc-4866-952b-aa1c3ebfb310)


## 5. 프로젝트 후기

#### 이동호
- CV Engineer를 목표로 하는 저에게는 너무 중요한 기회였기 때문에 이번에 제대로 이해하고 넘어가는 것을 목표로 했었습니다. 
- 기존에 제가 알던 지식을 더해 한 단계 성장한 것 같아 기쁩니다.

#### 김이준
- 이번 경진대회때 WandB를 처음 적용해봤는데 팀원끼리 공유도 가능하고 실시간 로그도 보여서 다음 프로젝트때도 초반부터 도입하면 좋을것같다.
- 그리고  팀원분들과 같이 다양한 방법을 시도해서 좋았다.

#### 박주연
- 팀원분들의 역량과 열정이 뛰어나서 많이 배울 수 있는 시간이었습니다. 
- 이번 경험을 통해 CV 분야에 대해 좀더 관심을 가지고 공부하고 싶습니다.

#### 마서연
- 팀원분들이 진행상황이라던지 해 본 시도들이라던지 여러모로 소통과 공유를 잘해주셔서 많은 걸 배웠다. 
- 대회 중반부터는 남들에 비해서 내가 개인적으로 한 점수들이 안오르길래 고민을 많이 했는데, 그래도 팀원분들 덕에 대회를 잘 마무리 한 것 같아 감사하다.

