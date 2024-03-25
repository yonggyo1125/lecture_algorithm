# 알고리즘이란?

## 세 값의 최댓값

```java
package chap01;
import java.util.Scanner;

public class Max3 {
    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);

        System.out.println("세 정수의 최댓값을 구합니다.");
        System.out.print("a의 값 : "); int a = stdIn.nextInt();
        System.out.print("b의 값 : "); int b = stdIn.nextInt();
        System.out.print("c의 값 : "); int c = stdIn.nextInt();

        /* a,b,c의 최대값을 구하여 max에 대입 */
        int max = a;
        if (b > max) max = b;
        if (c > max) max = c;
    
        System.out.println("최대값은 " + max "입니다.");
    }
}
```

- 최대값을 구하는 과정
    - max에 a 값을 넣는다. 
    - b값이 max보다 크면 max에 b값을 넣는다. 
    - c값이 max보다 크면 max에 c값을 넣는다.
- 여러 문장이 순차적으로 실행되는 구조를 순차적(concatenation)구조라고 합니다.
- ()안의 식의 평가 결과에 따라 프로그램의 실행 흐름을 변경하는 if문을 선택(selection)구조라고 합니다.


## 세 값의 중앙값 


##  조건 판단과 분기


## 순서도(flow chart)의 기호

> 문제에 대한 정의, 분석, 해법을 그림으로 표현하느 것

### 프로그램의 순서도


#### 데이터(data)

![image1](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/1.png)

- 데이터의 입력과 출력을 나타냅니다. 



#### 처리(process)

![image2](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/2.png)

- 여러 종류의 처리 기능을 수행합니다. 
- 정보의 값, 자료형, 위치를 바꾸도록 정의한 연산이나 연산집합의 실행 또는 연속적인 몇 가지 흐름 가운데 하나의 방향을 결정하는 연산집합이나 연산군의 실행을 나타냅니다.


#### 미리 정의한 처리(predefined process)

![image3](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/3.png)

- 서브 루틴 및 모듈 등 다른 곳에서 이미 정의한 하나 이상의 연산 또는 명령어들로 이루어진 처리를 나타냅니다.


#### 판단(decision)

![image4](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/4.png)

- 하나의 입구와 하나 이상을 선택할 수 있는 출구가 있고 기호에서 정의한 조건을 평가하여 하나의 출구를 선택하는 판단기능(스위치형 기능)을 나타냅니다.
- 주로 예상되는 평가 결과의 경로를 선 가까이에 씁니다.

#### 루프 범위(loop limit)

![image5](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/5.png)

- 두 부분으로 구성되어 루프의 시작과 종료를 나타냅니다.
- 기호의 두 부분에는 같은 이름(루프에 대한 임의의 이름)을 사용합니다. 
- 루프의 시작 기호(반복 전에 판단하는 경우) 또는 종료 기호(반복 후 판단하는 경우)안에 초깃값(초기화), 증가값, 종료값(종료 조건)을 표기합니다.

![image6](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/6.png)

> 변수 i를 1번 부터 n까지 1씩 증가하면서, <code>처리</code>를 n번 반복하는 순서도 입니다. '1,1,n' 대신 '1,2,..., n'을 사용하기도 합니다.

#### 선(line)

![image7](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/7.png)

- 제어의 흐름을 나타냅니다. 
- 주로 흐름의 방향을 분명히 나타내고자 할 때 화살표를 붙이는데, 순서도에 작성할 때도 보기 쉽게 화살표를 붙이기도 합니다.

#### 단말(terminator)

![image8](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/8.png)

- 외부 환경으로 나가거나 외부 환경에서 들어오는 것을 나타냅니다. 
- 프로그램 흐름의 시작과 종료를 나타냅니다.

> 선 종류별 설명
> 
> **실선(real line)** : 끊어진 곳 없이 이어진 선<br>
> **점선(dotted line)** : 일정한 간격으로 점을 찍어 이어진 선<br>
> **파선(broken line)** : 긴 선과 짧은 선은 3:1 비율로 이은 선


---
# 반복