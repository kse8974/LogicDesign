# Lab 09
## 실습 내용
### ****적외선 컨트롤러(IR Controller)를 이용하여 통신****


### **Modelsim에서 학습할 것**

**:  top코드를 작성하여 Simulate 돌려서 wave 확인하기**

**: Wave에서 리모컨 송신시호에서 Leader Code, Custom Code(16bit), Data Code(16bit)이 들어오는 것 확인하기**

**: Leader Code는 1로 9ms 들어오고 0으로 4.5ms가 들어오는 것을 확인**

**:Custom Code는 특정회사별로 다르게 나타남.**

**: Data Code는 송신데이터로 Bit 0 은 그림1, Bit 1은 그림2 와 같은 신호의 길이가 들어왔을 때를 의미함.**

![](https://github.com/kse8974/LogicDesign/blob/master/09/figs/bit%20.jpg)


## 결과(WAVE 해석과 코드해석)

**: Quartus에서 확인해본 회로**

![](https://github.com/kse8974/LogicDesign/blob/master/09/figs/circuit.jpg)

**: WAVE 해석**

![](https://github.com/kse8974/LogicDesign/blob/master/09/figs/wave1.jpg)

![](https://github.com/kse8974/LogicDesign/blob/master/09/figs/wave3.jpg)

위에 wave 형태를 먼저 살펴보도록 하자.
사전지식으로 리모콘 송신신호는 Leader Code, Custom Code, Data Code가 있다는 것을 알고있다고 보자.

먼저 Leader Code의 wave를 살펴보면
Leader Code는 1로 9ms 들어오고 0으로 4.5ms가 들어오는 것을 확인하기 위해서는 1ms단위로 신호가 들어오는 것을 확인해야하기 때문에 1M clk을 만들어줘야한다. 따라서 nco 모듈을 이용하여 1M clk을 만들어 준다. clk_h가 0-8999까지 올라가는 것과 clk_l이 0인 상태가 유지되면 Leader Code에서 1로 9ms가 들어오는 상태인 것을 알 수 있다. 또한 그림1에서 커서를 통해 그 시간이 8.98516ms라는 것을 알 수 있다. 이와 마찬가지로 clk_h=0 이고 clk_l이 0-4499까지 올라갈 때는 Leader Code에서 0으로 4.5ms가 들어오는 상태라는 것을 알 수 있다. 

다음으로 Custom Code의 wave를 살펴보면






<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MDE0OTE3NDUsLTIxNzMxMDkxNCwtMj
IyNjk4MzAyLDEzODk3NDE3MDddfQ==
-->