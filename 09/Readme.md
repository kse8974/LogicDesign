# Lab 09
## 실습 내용
### ****적외선 컨트롤러(IR Controller)를 이용하여 통신****


### Modelsim에서 학습할 것

**:  top코드를 작성하여 Simulate 돌려서 wave 확인하기**

**: Wave에서 리모컨 송신시호에서 Leader Code, Custom Code(16bit), Data Code(16bit)이 들어오는 것 확인하기**

**: Leader Code는 1로 9ms 들어오고 0으로 4.5ms가 들어오는 것을 확인**

**:Custom Code는 특정회사별로 다르게 나타남.**

**: Data Code는 송신데이터로 Bit 0 은 그림1, Bit 1은 그림2 와 같은 신호의 길이가 들어왔을 때를 의미함.**

![] (https://github.com/kse8974/LogicDesign/blob/master/09/figs/bit%20.jpg)


## 결과(WAVE 해석과 코드해석)

**: WAVE 해석

![]

**:  설정모드에서 7-segment의 dp를 활용한 설계**
* 예) 초 설정 시 - 초 부분의 dp led 점등

**:  Blink 모드 개발**
* 설정모드에서 설정부분을 깜빡이게 display



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIyMjY5ODMwMiwxMzg5NzQxNzA3XX0=
-->
