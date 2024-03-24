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





---
# 반복