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


# 클래스
