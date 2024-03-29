# AutoLayout Rect
AutoLayout Recture

1강 기초
===========
## A. Constaraint
뷰의 하나의 값에 대한 제약사항 이다. 예를 들어, 뷰의 중심은 X방향으로 SuperView의 중심과 같아야한다.

1. Leading
2. Trailing
3. Top
4. Bottom

*. Error : 정확한 위치와 크기를 잡을 수 없을때 에러 발생한다.

## B. Safe Area
아이폰 X경우 상하단은 사용하지 말라는 것, 가로모드의 하단 제스쳐를 사용하지 말라는 것 등의 시스템 영역을 사용하는 부분을 디자인 적으로 사용하지 말라는 것

## C. Equal

* 여러개의 오브젝트의 width, height를 똑같이 가져가는 방식

* equal의 constant 값을 20으로 준다면 크기를 +20 가져 간다는 의미이다.

<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202019-06-19%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2012.28.26%202.png" width = 350 height = 200>

* 예제) 화면 두개를 꽉 채우기

<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/1.png" width = 200 height = 450> <img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/2.png" width = 200 height = 150>  <img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/3.png" width = 200 height = 150>

## D. Align

* 어떤 뷰를 기준으로 정렬 하는 것

1. Horizontal in Container, Vertical in Container : 부모 뷰 기준으로 수평, 수직 정렬
2. Horizontal Center, Vertical Center : 어떤 뷰 기준으로 수평, 수직 정렬
3. Ledaing, Trailing, Bottom, Edge : 어떤 뷰 기준으로 좌, 끝, 아래, 상단 정렬

## E. Multiplier

* 어떤 화면의 Constraint에 대한 비율이다, 2, 2%, 1:2, 1/2 처럼 표현 할 수 있다.

* Top과 Leading의 계산법

          Y * 2 + 10

* Bottom 과 Trailing 의 계산법

          818 = 2 * X + 10, 이들의 계산이 다른 것은 끝을 나타내는 속성을 가지기 때문이다.

* 예제) leading multiplier 2

          Top에 * 2를 하여 현재 y 값에 * 2를 하게 된다. iPhone X 경우 상단 44 공간이 있기 때문에 * 2 = 88


<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/4.png" width = 250 height = 550> <img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/5.png" width = 250 height = 200> <img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/6.png" width = 250 height = 100>

* 예제) leading multiplier 2 + 10

          Top에 * 2를 하여 현재 y 값에 * 2를 하게 된다. 그리고 constant 10을 주면 그만큼 10 더한 98의 상단 여백을 가지게 된다.

* 예제) Bottom multipier 2

          818 = height * 2 이기 때문에 height가 절반이 줄게 된다.
          
* 예제) 이미지 중앙이 아닌 살짝 상단에 위치한 라벨 그리기

          Algin Center Y Mutiplier * 0.6 > 40% 정도 상단으로 올려준다.

<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/7.png" width = 250 height = 550>
         
         
* 예제) 뷰 4개를 일정하게 배치 하기

          Algin Center Y,X to SuperView 1.5 or 0.5

<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/9.png" width = 250 height = 550>


## E. Priority

* 우선순위가 높다는 것은 우선 반영 된다는 의미이다. 낮다는것 나중에 반영

* Content Hugging Priority : 내가 가진 컨텐츠를 그대로 노출 시킬 수 있는 가에 대한 우선순위, 더 높은 우선순위를 가진 Label이 Fit하게 설정된다.

* Compression Resistance Priority : 현재 Label이 주변 Label에 의해 찌그려지는 정도를 낮추는 거에 대한 우선순위 더 높은 우선순위 가진 Label이 찌그러짐 정도 가 낮다.

* Line Break : 짤리는 부분에 대한 표현 법

* intrinsic Content Size : 본질적인 컨텐츠 크기

## F. Vary for traits

* 화면의 상태에 따라(가로모드, 세로모드)혹은 특정 디바이스에 따라서 적용되는 AutoLayout 을 설정

1. Vary for Traits 선택 height, width에 따라서 적용되는 모드 선택
2. height를 선택하면 landscape에 적용되는 모델들 확인 가능
3. 변경될 AutoLayout을 지정하고 Constraints값들을 변경한 후 Done시 완료

## G. MARGIN

* 부모 뷰와 자식 뷰간의 간격

1. Add New Constraints에 Constrain to margins 선택
<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/11.png" width = 150 height = 200>

2. layout margin을 선택하여 default, fixed, language directional 선택하여 margin 조절
<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/10.png" width = 150 height = 200>

## H. StackView

* 연속된 뷰들을 간단하게 표현이 가능
<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/12.png" width = 150 height = 250>

1. Axis : 스택뷰의 방향

2. Alignment : 오브젝트들의 스택뷰 안에서의 방향

          * Axis가 Horizontal 인 경우 : Fill, Top, Center, Bottom
          * Axis가 Vertical 인 경우 : Fill, Leading, Center, Trailing

3. Distribution : 오브젝트들 간 어떻게 표현 할지 설정

          * Fill
          * Fill Equally
          * Fill Proportionally
          * Equal Spacing
          * Equal Centering : 각 뷰의 센터간 간격이 Spacing 값
