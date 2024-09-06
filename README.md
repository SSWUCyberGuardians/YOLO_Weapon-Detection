# YOLOv8_Weapon-Detection

## I. Introduction
공공 안전 강화를 위한 딥러닝 기반의 무기 소지 탐지와 감정 분석 기법에 관한 프로젝트입니다.
본 연구는 칼, 권총, 배트, 총기 등 무기류의 범위를 넓혀 데이터셋을 구축 하고 YOLOv8로 학습시켜 범죄 예측 및 대응 능력을 강화했습니다. 기존의 객체 탐지 모델은 ‘사람’, ‘총’, ‘칼’ 등을 개별적으로 탐지하는 데는 효과적이었으나, ‘총을 든 사람’이나 ‘칼을 든 사람’과 같은 복합 객체의 탐지는 미흡했습니다. 본 연구는 이러한 한계를 극복하기 위해 사람과 무기가 결합된 이미지로 학습하는 방식을 채택하여 복합적인 상황에서도 높은 정확도로 무기 소지자를 탐지할 수 있도록 데이터셋을 최적화했습니다.

또한, 실제 환경과 CCTV 영상 사이에 존재하는 차이에 주목하여 'CCTV 영상 내 무기 소지자 캡쳐본' 사진 데이터셋을 추가로 활용하여 학습을 진행해 2차원 비디오 내에서 무기 소지자를 보다 정확하게 탐지할 수 있는 방법론을 개발했습니다.

---

## II. Demo
<div style="display: flex; justify-content: space-between;">
    <img width="45%" src="https://github.com/user-attachments/assets/3dd810f2-2c49-4eb8-8ad9-4d9e80076f62" alt="Demo Image 1"/>
    <img width="45%" src="https://github.com/user-attachments/assets/83486e1a-0f8c-46d0-9287-1c2eb1420862" alt="Demo Image 2"/>
</div>

---

## III. Best Model Validation Result
<img width="100%" alt="Validation Result" src="https://github.com/user-attachments/assets/e756121b-d5e7-41b4-873d-63a2e59033c3"/>

---
## IV. Dataset
- 'Weapon Dataset'과 'Person Dataset'은 주로 Roboflow에서 제공하는 이미지 데이터를 활용하여 합쳤고, 일부는 Open Images V7 에서 무작위로 선별한 데이터를 사용하여 데이터셋을 구축하였습니다.
-  Weapon Dataset은 칼, 배 트, 권총, 총기가 Weapon으로 포함되어 있으며, 사람도 하나의 카테고리로 분류해 {person : 0, weapon : 1}로 라벨링 하였습니다.
    - test dataset : 301
    - train dataset : 1211
    - val dataset : 103

 ---
 ### Result of Object Detection
<img width="395" alt="image" src="https://github.com/user-attachments/assets/03a79acd-b373-4ae3-91d6-03e60b7e76a0">

