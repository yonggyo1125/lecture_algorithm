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

## 1부터 n까지 정수 합 구하기 

```java
package chap01;
import java.util.Scanner;

public class SumWhile {
    public static void main(String[] args) {
        Scanner stdIn = new Scanner(Systen.in);

        System.out.println("1부터 n까지의 합을 구합니다.");
        System.out.println("n의 값: ");
        int n = stdIn.nextInt();

        int sum = 0;
        int i = 1;

        while (i <= n) {
            sum += i;
            i++;
        }
        System.out.println("1부터 " + n + "까지의 합은 " + sum + "입니다.");
    }
}
```

### while문 반복 

- while문은 실행 전에 반복을 계속할지 판단
- **사전 판단 반복 구조**라고 부릅니다.


### for문 반복

> 하나의 변수를 사용하는 반복문은 while문보다 for문을 사용하는 것이 좋다.

```java
package chap01;
import java.util.Scanner;

public class SumFor {
    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);

        System.out.println("1부터 n까지의 합을 구합니다.");
        System.out.print("n의 값 : ");
        int n = stdIn.nextInt();

        int sum = 0;

        for(int i = 1; i <= n; i++)
            sum += i;
        
        System.out.println("1부터 " + n + "까지의 합은 " + sum + "입니다.");
    }
}
```

## 양수만 입력하기 

```java
import chap01;
import java.util.Scanner;

public class SumForPos {
    Scanner stdIn = new Scanner(System.in);
    int n;

    System.out.println("1부터 n까지의 합을 구합니다.");

    do {
        System.out.println("n의 값: ");
        n = stdIn.nextInt();
    } while (n <= 0);

    int sum = 0;

    for (int i = 1; i <= n; i++) 
        sum += i;
    
    System.out.println("1부터 " + n + "까지의 합은 " + sum + "입니다.");
}
```

- do문은 루프 본문을 한 번 실행한 다음에 계속 반복할 것인지를 판단하는 **사후 판단 반복문** 입니다. 
- while문과 마찬기지로 ()안의 제어식을 평가한 값이 0이 아니면 루프 본문의 명령문이 반복됩니다.


> 사전 판단 반복과 사후 판단 반복의 차이점
>
> 사전 판단 반복문인 while문과 for문은 처음에 제어식을 평가한 결과가 0이면 루프 본문은 한 번도 실행되지 않습니다. 이와 달리 반복문인 do문은 루프 본문이 반드시 한번은 실행됩니다. 

## 구조적 프로그래밍(structured programming)

- 하나의 입구와 하나의 출구를 가진 구성 요소만을 계층적으로 배치하여 프로그램을 구성하는 방법
- 순차, 선택, 반복이라는 3종류의 제어 흐름을 사용


```java
package chap01;
import java.util.Scanner;

public class Digits {
    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);
        int no;

        System.out.println("2자리의 정수를 입력하세요.");

        do {
            System.out.print("입력: ");
            no = stdIn.nextInt();
        } while (no < 10 || no > 99);

        System.out.println("변수 no의 값은 " + no + "가(이) 되었습니다.");
    }
}
```

### 논리 연산자의 단락회로 평가 

> 논리 연산의 식 전체를 평가한 결과가 왼쪽 피연산자의 평가 결과만으로 정확해지는 경우 오른쪽 피연산자의 평가를 수행하지 않는 것 

### 드모르간 법칙(De Morgan's laws)

- 논리 부정 연산자는 피연산자가 true면 false를, false면 true를 반환하는 단항 연산자
- 각 조건을 부정하고 논리곱을 논리합으로, 논리합을 논리곱으로 바꾸고 다시 전체를 부정하면 원래의 조건과 같다. 
- x && y와 !(!x || !y)는 같습니다.
- x || y와 !(!x && !y)는 같습니다.

```
no < 10 || no > 99 조건은 !(no >= 10 && no <= 99)와 같다.
```

![image9](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/9.png)


## 다중 루프 

- 반복문 안에서 다시 반복할 수 있습니다.
- 반복 루프가 중첩되는 수준에 따라 **이중 루프, 삼중 루프**라고 합니다.

### 곱셈표

```java
package chap01;

public class Multi99Table {
    public static void main(String[] args) {
        System.out.println("---- 곱셈표 ----");

        for (int i = 1; i <= 9; i++) {
            for (int j = 1; j <= 9; j++) {
                System.out.printf("%3d", i * j);
            }
            System.out.println();
        }
    }
}
```

![image10](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/10.png)

> 곱셈표를 출력하는 순서도

## 직각 이등변 삼각형 출력 


```java
package chap01;
import java.util.Scanner;

public class TriangleLB {
    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);
        int n;

        System.out.println("왼쪽 아래가 직각인 이등변 삼각형을 출력합니다.");

        do {
            System.out.print("몇 단 삼각형입니까? : ");
            n = stdIn.nextInt();
        } while(n <= 0>);

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

- 삼각형을 위부터 1행 ~ n행이라고 하면 i행에 i개의 기호 문자 *를 출력하고 마지막 n행에 n개의 기호 문자 *를 출력합니다.

![image11](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/11.png)
