### 네 값의 최댓갑을 구하는 max4 메서드를 작성하시오.

```java
static int max4(int a, int b, int c, int d)
```

--- 
### 세 값의 최솟값을 구하는 min3 메서드를 작성하시오.

```java
static int min3(int a, int b, int c)
```

### 네 값의 최솟값을 구하는 min4 메서드를 작성하세요.

```java
static int min4(int a, int b, int c, int d)
```

### n이 7이면 '1 + 2 + 3 + 4 + 5 + 6 + 7 = 28'로 출력하는 프로그램을 작성하시오.

```
```

### 1부터 10까지의 합은 (1 + 10) * 5와 같은 방법으로 구할 수 있습니다. 가우스 덧셈이라는 방법을 이용하여 1부터 n까지의 정수 합을 구하는 프로그램을 작성하세요.

```
```

### 정수 a,b를 포함하여 그 사이의 모든 정수의 합을 구하여 반환하는 아래 메서드를 작성하세요.

> a와 b의 대소 관계에 상관없이 합을 구하세요(a가 3, b가 5면 12, a가 6, b가 4면 16)

```java
static int sumof(int a, int b)
```


### 다음과 같이 위쪽과 왼쪽에 곱하는 수가 있는 곱셈표를 출력하는 프로그램을 작성하세요.
> 구분선은 수직선 기로(|), 마이너스 기호(-), 플러스 기호(+)를 사용하세요.


![image12](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/12.png)


## 곱셈이 아니라 덧셈을 출력하는 프로그램을 작성하세요.
> 곱셈표와 같이 표의 위쪽과 왼쪽에 더하는 수를 출력하세요.

### 다음과 같이 입력한 수를 한 변으로 하는 정사각형을 *기호로 출력하는 프로그램을 작성하세요.

![image13](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/13.png)


### 직각 이등변 삼각형을 출력하는 부분을 아래와 같은 형식의 메서드로 작성하세요.

```java
static void triangleLB(int n)  // 왼쪽 아래가 직각인 이등변 삼각형을 출력 
```

- 또 외쪽 위, 오른쪽 아래가 직각인 이등변 삼각형을 출력하는 메서드를 작성하세요.

```java
static void triangleLU(int n)   // 왼쪽 위가 직각인 이등변 삼각형을 출력
static void triangleRU(int n)   // 오른쪽 위가 직각인 이등변 삼각형을 출력
static void triangleRB(int n)   // 오른쪽 아래가 직각인 이등변 삼각형을 출력
```

### n단의 피라미드를 출력하는 메서드를 작성하세요. 

![image14](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/14.png)


```java
static void spira(int n)
```

> i행에는 (i - 1) * 2 + 1개의 기호문자 * 가 출력되게 하세요(마지막 n행에는 (n-1) * 2 + 1개의 기호문자 *를 출력하게 됩니다.)


### 다음과 같이 아래를 향한 n단의 숫자 피라미드를 출력하는 메서드를 작성하세요.

![image15](https://raw.githubusercontent.com/yonggyo1125/lecture_algorithm/master/01%20%EA%B8%B0%EB%B3%B8%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98/images/15.png)


```java
static void npira(int n)
```

> i행에 출력하는 숫자는 i % 10으로 구하세요.