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

* 예제 화면 두개를 꽉 채우기
<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/1.png" width = 250 height = 550>
<img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/2.png" width = 150 height = 100> <img src = "https://github.com/HwangWoonChun/AutoLayout/blob/master/3.png" width = 150 height = 100>
