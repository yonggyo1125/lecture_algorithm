# 배열 

## 자료구조

- 데이터 단위와 데이터 자체 사이의 물리적 또는 논리적인 관계
- **데이터 단위**: 데이터를 구성하는 한 덩어리
- **자료구조**: 자료를 효율적으로 이용할 수 있도록 컴퓨터에 저장하는 방법

## 배열

- 같은 자료형의 변수로 이루어진 구성 요소(component)가 모인 것 

```java
int[] a; // a는 자료형이 int형인 배열: 형식 A
int a[]; // a는 자료형이 int형인 배열: 형식 B
```
> 단순한 int형이 아니라 int형인 배열임을 명확하게 나타내는 형식 A쪽을 훨씬 많이 사용 

- 자료형이 int이고 구성 요소의 개수가 5개인 배열 

```java
a = new int[5]; 
```
> int형의 배열 본체를 생성하고 그것을 변수 a가 **참조**하도록 설정한다는 것 

![image1](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/1.png)

> 배열의 구성 요소는 자동으로 0으로 초기화되는 규칙이 있음 

### 구성 요소 

- 배열 안의 모든 구성 요소의 형은 같고 직선 모양으로 줄지어 있습니다. 
- **연산자 []** :  배열의 개별 요소에 접근하기 위해 사용하는 연산자 
- 첫 번째 열 요소의 인덱스는 0으로 정해져 있습니다.
- 구성 요소에 접근하는 식은 순서대로 a[0], a[1], a[2], a[3], a[4] 입니다. 

```
배열 변수 이름[인덱스]  
```
> 구성 요소가 n개인 배열 구성 요소는 a[0], a[1], ..., a[n-1]입니다. a[n]은 존재하지 않습니다.

### 구성 요소수(길이)

- 배열 본체와 함게 구성 요소 개수인 length라는 변수가 만들어집니다. 

```
배열 변수 이름.length
```

### 기본값 

```java
package chap02

public class IntArray {
    public static void main(String[] args) {
        int[] a = new int[5];  // 배열의 선언

        a[1] = 37;   // a[1]에 37 대입
        a[2] = 51;   // a[2]에 51 대입 
        a[4] = a[1] * 2;   // a[4]에 a[1] * 2, 즉 74 대입

        for (int i = 0; i < a.length; i++) {
            System.out.println("a[" + i + "] = " + a[i]);
        }
    }
}
```

```
실행 결과 
a[0] = 0
a[1] = 37
a[2] = 51
a[3] = 0
a[4] = 74
```
> 배열의 자료형
>
> 배열 a의 각 요소의 자료형은 int형 배열이고 배열 a의 자료형은 int[5]형 입니다. 다시말해 a[0]은 int형, a는 int[5]형 입니다.<br>
> 예를 들어 int a = new int[5]라고 선언하면 배열 a는 a[0], a[1], a[2], a[3], a[4]로 총 5개의 저장 공간을 차지합니다.

```java
int[] a; // 선언하기
a = new int[3]; // 참조하기 
```

![image2](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/2.png)


### 배열의 초기값 

|형|초기값|
|---|-----|
|byte|(byte)0|
|short|(short)0|
|int|0|
|long|0L|
|float|0.0f|
|double|0.0|
|char|'\u0000'|
|boolean|false|
|참조형|null|


> [참고]값을 대입하지 않은 지역 변수 
>
> 메서드 안에 선언한 지역 변수는 초깃값으로 초기화되지 않습니다. 즉, 변수를 만들어도 초기화는 수행되지 않습니다. java에서는 초기화나 대입에 의해 값이 넣어져 있지 않은 변수로부터는 값을 꺼낼 수 없습니다. 따라서 다음 프로그램은 컴파일 오류가 발생합니다.

```java
int a;  //  값이 들어 있지 않은 변수에서 값을 꺼내려고 합니다.
System.out.println("a 값은 " + a + "입니다."); // 컴파일 오류
```

### 배열 요소값을 초기화하여 배열 선언하기 

- 배열 본체의 생성과 동시에 각 요소의 초기화가 가능 

```java
package chap02;

public class IntArrayInit {
    public static void main(String[] args) {
        int[] a = {1, 2, 3, 4, 5}; // 배열 초기화에 의해 생성

        for (int i = 0; i < a.length; i++) {
            System.out.println("a[" + i + "] = " + a[i]);
        }
    }
}
```


### 배열의 복제

```
배열이름.clone()
```

```java
package chap02;

public class CloneArray {
    public static void main(String[] args) {
        int[] a = {1, 2, 3, 4, 5};
        int[] b = a.clone();   // b는 a의 복제를 참조

        b[3] = 0; 

        System.out.print("a = ");
        for (int i = 0; i < a.length; i++) {
            System.out.print(" " + a[i]);
        }

        System.out.print("\nb = ");
        for(int i = 0; i < b.length; i++) {
            System.out.print(" " + b[i]);
        }
    }
}
```


```
실행 경과
a = 1 2 3 4 5
b = 1 2 3 0 4
```

![image3](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/3.png)


## 배열 요소의 최댓값 구하기

- 배열 a의 요소가 3개일 때 세 요소 a[0], a[1], a[2] 중 최댓값은 아래 프로그램처럼 구할 수 있습니다.

```java
max = a[0];
if (a[1] > max) max = a[1];
if (a[2] > max) max = a[2];  
```
> 요소 개수가 3개이면 if문을 2개 작성합니다.

- 요소가 4개이면 아래처럼 해야 합니다.

```java
max = a[0];
if (a[1] > max) max = a[1];
if (a[2] > max) max = a[2];
if (a[3] > max) max = a[3];
```
> 요소 개수가 4개이면 if문을 3개 작성합니다.

- a[0], a[1], ..., a[n-1]의 최댓값을 구하는 프로그램은 아래처럼 구현할 수 있습니다.

```java
max = a[0];
for (i < 1; i < n; i++) {
    if (a[i] > max) max = a[i];
}
```
> 요소 개수가 n개이면 if문을 n-1개 작성합니다.

![image4](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/4.png)

- 방금 작성한 알고리즘에 따라 배열 a의 요소에서 최댓값을 구하는 과정은 다음과 같습니다.

![image5](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/5.png)

> 스캔 과정에서 if문의 제어식 a[i] > max가 참일 때(살펴보고 있는 요소 a[i]의 값이 최댓값 max보다 클 때) a[i]의 값을 max에 대입합니다. 결과적으로 배열의 모든 요소에 대해 스캔을 완료한 시점의 배열 a의 최대 요솟값은 max에 대입됩니다.

### 배열 요소의 최대값을 구하는 메서드

```java
package chap02;
import java.util.Scanner;

public class MaxOfArray {
    public static int maxOf(int[] a) {
        int max = a[0];
        for (int i = 1; i < a.length; i++) {
            if (a[i] > max)
                max = a[i];
        }

        return max;
    }

    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);

        System.out.println("키의 최댓값을 구합니다.");
        System.out.print("사람 수 : ");
        int num = stdIn.nextInt(); // 배열의 갯수를 입력 받음 

        int[] height = new int[num]; // 배열의 갯수가 num인 배열을 생성

        for (int i = 0; i < num; i++) {
            System.out.print("height[" + i + "]:");
            height[i] = stdIn.nextInt();
        }

        System.out.println("최댓값은 " + maxOf(height) + "입니다.");
    }
}
```

```
실행 결과 

키의 최대값을 구합니다.
사람 수 : 5
height[0]: 172
height[1]: 153
height[2]: 192
height[3]: 140
height[4]: 165
최대값은 192입니다.
```

![image6](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/6.png)

> 인수 height는 배열 본체를 참조하는 배열 변수입니다. 따라서 메서드 maxOf에 전달하는 것은 **배열 본체에 대한 참조**입니다. 호출한 메서드 maxOf에서는 배열 변수인 매개변수 a가 전달받은 참조로 초기화되므로 배열 변수 a는 배열 height의 본체를 참조합니다. 그 결과 메서드 maxOf 안의 배열 a는 사실상 main 메서드의 배열 height인 것입니다. 이런 원리로 배열을 전달하므로 메서드 maxOf 안에서는 전달받은 a.length로 얻을 수가 있고 각 요소를 a[i]로 액세스 할 수 있습니다.

### 난수 사용해 배열 요소값 설정하기 

```java
package chap02;
import java.util.Random; // (1)
import java.util.Scanner;

public class MaxOfArrayRand {
    public static int maxOf(int[] a) {
        int max = a[0];
        for (int i = 1; i < a.length; i++) {
            if (a[i] > max) {
                max = a[i];
            }
        }

        return max;
    }

    public static void main(String[] args) {
        Random rand = new Random(); // (2)
        Scanner stdIn = new Scanner(System.in);

        System.out.pritnln("키의 최대값을 구합니다.");
        Systen.out.print("사람 수 : ");
        int num = stdIn.nextInt(); // 배열의 요소수를 입력받음
 
        int[] height = new int[num]; // 요소수가 num인 배열을 생성

        System.out.println("키 값은 아래와 같습니다.");
        for (int i = 0; i < num; i++) {
            height[i] = 100 + rand.nextInt(90); // 요소의 값을 난수로 결정 - (3)
        }

        System.out.println("최댓값은 " + maxOf(height) + "입니다.");
    }
}
```
> 사람 수를 입력하면 곧바로 그 사람 수만큼 키의 값이 자동으로 생성되고 최댓값이 출력됩니다.

- 난수를 생성할 때 java.util 패키지의 Random 클래스를 사용합니다.
- 난수를 생성하는 단계 
    - (1) Random 클래스를 간단한 이름으로 사용하기 위해 import 선언을 합니다.
    - (2) Random 클래스형의 변수(이 프로그램에서는 rand)를 만들기 위한 선언을 합니다.
    - (3) 변수 rand에 대한 난수를 생성하는 메서드 nextInt를 호출합니다.
- nextInt(n)가 반환하는 것은 0부터 n - 1 까지의 난수입니다. 이 프로그램의 경우 0부터 89까지의 난수가 생성됩니다.

> 진짜 난수, 의사 난수
>
> 로또 복권에서 번호가 적힌 공을 손으로 하나하나 꺼내 당첨번호를 결정하는 과정은 '진짜 난수'를 생성합니다. 의사 난수에서 의사는 실제와 비슷하다는 뜻입니다.

> 컴퓨터에서 생성하는 난수는 진짜 난수가 아닙니다.
>
> 컴퓨터 과학에서 난수는 보통 특정 입력값이나 컴퓨터 환경에 따라 무작위로 선택한 것처럼 보이는 난수를 생성합니다. 그런데 srand 메서드에 전달한 seed(씨앗)의 값과 컴퓨터 환경이 같다면 그 결과값은 항상 같습니다. 결국 컴퓨터에서 생성된 모든 난수는 미리 컴퓨터가 계산해 둔 의사난수 입니다. 컴퓨터는 계산된 결과만 가지고 난수를 생성하는데, 이 계산된 결과는 입력값에 의해 결저오디므로 이 값으로 임의의 난수를 생성할 수는 없습니다(컴퓨터를 처음 켜면 난수표를 생성하여 보관한다고 생각하면 됩니다).
>
> seed(씨앗값) 1을 넣은 경우의 예: 항상 1 -> 105 -> 999 -> 1002 ...의 순서로 숫자를 생성<br>
> seed(씨앗값) 2를 넣은 경우의 예: 항상 2 -> 892 -> 7291 -> 10123 ...의 순서로 숫자를 생성 
> ...
> 
> 따라서 프로그램에서 매번 같은 방법(같은 seed(씨앗)을 사용해)으로 난수를 가져오면 처음 실행할 떄 이외에는 난수라고 할 수 없습니다. 그래서 보통 seed(씨앗)라 불리는 수를 srand 메서드에 매개변수로 매번 다르게 전달해 항상 다른 의사 난수를 생성해야 합니다. 이때 seed(씨앗) 값을 항상 다르게 주기 위해 현재 시간을 이용하는 것이 일반적입니다. 현재 시간은 매 순간마다 바뀌므로 이전에 발생한 의사 난수를 다시 생성하지는 않습니다.

## 배열 요소를 역순으로 정렬하기 

- 다음은 순서를 뒤바꾸는 과정을 나타낸 그림입니다.

![image7](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/7.png)
> 배열의 요소를 역순으로 정렬

- 교환 횟수는 **요소 갯수/2**이며 이 나눗셈에서 나머지는 버립니다. 위 예제에서 볼 수 있듯이 요소 개수가 홀수인 경우 가운데 요소는 교환할 필요가 없기 때문입니다.
> 정수/정수 연산은 나머지를 버리고 정수부만 얻을 수 있으므로 나머지를 버리기에 좋습니다(요소 개수가 7인 경우 교환 횟수는 7/2, 곧 3입니다).

- 요소 개수가 n개인 배열 요소를 역순으로 정렬하는 알고리즘

```java
for (i = 0; i < n / 2; i++) {
    // a[i]와 a[n - i - 1]의 값을 교환
}
```

### 두 값의 교환 
- 배열의 역순 정렬은 교환이 총 n/2회 필요합니다. 


![image8](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/8.png)
> 두 값의 교환

- 여기서 사용하는 작업용 변수를 t라 하면 교환 과정은 아래와 같습니다.
    - x값을 t에 보관 
    - y값을 x에 대입 
    - t에 보관한 처음 x값을 y에 대입

```java
t = a[idx1];
a[idx1] = a[idx2];
a[idx2] = t;
```


```java
public static void swap(int[] a, int idx1, int idx2) {
    int t = a[idx1]; a[idx1] = a[idx2]; a[idx2] = t;  // a[idx1]과 a[idx2]의 값을 교환
}
```

```java
package chap02;
import java.util.Scanner;

public class ReverseArray {
    public static void swap(int[] a, int idx1, int idx2) {
        int t = a[idx1]; a[idx1] = a[idx2]; a[idx2] = t;  // a[idx1]과 a[idx2]의 값을 교환
    }

    public static void reverse(int[] a) {
        for (int i = 0; i < a.length / 2; i++) {
            swap(a, i, a.length - i - 1);
        }
    }

    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);

        System.out.print("요솟수 : ");
        int num = stdIn.nextInt(); // 요솟수 

        int[] x = new int[num]; // 요솟수가 num인 배열

        for (int i = 0; i < num; i++) {
            System.out.print("x[" + i + "] : ");
            x[i] = stdIn.nextInt();
        }

        reverse(x); // 배열 a의 요소를 역순으로 정렬

        System.out.println("요소를 역순으로 정렬했습니다.");
        for (int i = 0; i < num; i++) {
            System.out.println("x[" + i + "] = " + x[i]);
        }
    }
}
```

## 두 배열의 비교
- 두 배열의 **모든 요소의 값이 같은가**를 판단하는 메서드를 구현한 프로그램입니다.

```java
package chap02;
import java.util.Scanner;

public class ArrayEqual {
    // 두 배열 a, b의 모든 요소가 같은가?
    public static boolean equals(int[] a, int[] b) {
        if (a.length != b.length) {  // (1)
            return false;
        }

        for (int i = 0; i < a.length; i++) { // (2)
            if (a[i] != b[i]) {
                return false;
            }
        }

        return true;  // (3)
    }

    public static void main(String[] args) {
        Scanner stdIn = new Scanner(System.in);

        System.out.print("배열 a의 요솟수 : ");
        int na = stdIn.nextInt(); // 배열 a의 요솟수

        int[] a = new int[na]; // 요솟수가 na인 배열

        for (int i = 0; i < na; i++) {
            System.out.print("a[" + i + "] : ");
            a[i] = stdIn.nextInt();
        }

        System.out.print("배열 b의 요솟수 : ");
        int nb = stdIn.nextInt(); // 배열 b의 요솟수
        
        int[] b = new int[nb]; // 요솟수가 nb인 배열

        for (int i = 0; i < nb; i++) {
            System.out.print("b[" + i + "] : ");
            b[i] = stdIn.nextInt();
        }

        System.out.println("배열 a와 b는 " + (equals(a, b) ? "같습니다." : "같지 않습니다."));
     }
}
```

- 두 배열 a, b의 모든 요소가 같은가의 판단은 아래처럼 세 단계로 수행합니다.
    - (1) 두 배열 a,b의 요솟수(길이)를 비교합니다. 요솟수가 다르면 배열이 같지 않다는 것이 분명합니다. - (a) 
    - (2) 이 for문에서는 두 배열을 처음부터 스캔하면서 요소 a[i]와 b[i]의 값을 비교하는 것을 반복합니다. 이 과정에서 값이 다른 요소를 발견하면 반환문을 실행하여 false를 반환합니다. - (b)
    - 프로그램의 흐름이 여기에 도달하면 for문이 중단되지 않고 끝까지 실행된 경우입니다. 두 배열은 같다고 판단할 수 있으므로 true를 반환합니다. - (c)

![image9](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/9.png)
> 두 배열의 비교

## 기수 변환 
- 10진수 정수를 n진수 정수로 변환하려면 정수를 n으로 나눈 나머지를 구하는 동시에 그 몫에 대해 나눗셈을 반복해야 합니다.
- 이 과정을 몫이 0이 될 때까지 반복하고, 이런 과정으로 구한 나머지를 거꾸로 늘어놓은 숫자가 기수로 변환한 숫자입니다. 

![image10](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/02%20%EA%B8%B0%EB%B3%B8%20%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0/images/10.png)

- 16진수는 아래 16의 문자로 표현되는 수입니다.

```
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

- 기수가 10단위를 넘는 경우 0 ~ 9에 이어지는 숫자로 알파벳 문자인 A, B, ...를 사용합니다. A, B, ...는 10진수의 10, 11, ...에 해당합니다. 

> 36진수는 숫자 0 ~ 9와 알파벳 A ~ Z를 이용하여 나타낼 수 있습니다.


> 정수 상수의 n진수 표현 방법
>
> 정수 상수는 정수 계열의 값을 나태내는 10진수(기수 10), 8진수(기수 8) 또는 16진수(기수 16)를 말합니다. 정수 상수는 변경할 수 없는 정수값을 나타낼 때 사용합니다. 정수 상수가 0x 또는 0X로 시작되는 경우는 16진수이고, 숫자 0으로 시작되는 경우 8진수입니다. 두 경우에 해당하지 않으면 10진수로 간주합니다.
>
> 0x1C  // 10진수 28에 대한 16진수 표기<br>
> 034   // 10진수 28에 대한 8진수 표기


```java
package chap02;
import java.util.Scanner;

public class CardConvRev {
    // 정수값 x를 r진수로 변환하여 배열 d에 아랫자리부터 넣어두고 자릿수를 반환합니다.
    
}
```



# 클래스
