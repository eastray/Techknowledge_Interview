#  etc..

### index

- if와 continue
- Ref




### if와 continue

continue 문은 반복문 내에서만 사용할 수 있으며, 진행 중인 반복문에서 continue 문을 만나면 반복문의 끝으로 이동하여 다음 반복이 진행된다. for 문의 경우 증감식으로 이동하며, while 문과 do ~ while 문의 경우 조건식으로 이동한다. Continue 문은 반복문 전체를 벗어나지 않고 다음 반복문을 계속 수행한다는 점이 break 문과 다르다. 주로 if 문과 함계 사용되어 특정 조건을 만족하는 경우 continue 문 이후의 문장들을 수행하지 않고 다음 반복으로 넘어가서 계속 진행하도록 한다. 전체 반복 중에 특정 조건을 만족하는 경우를 제외하고자 할 때 유용하다.

```java
class ifContinue {
  public static void main (String[] args) {
    for (int i = 0; i <= 10; i++){
      
      if (i % 3 == 0)
        continue;
      
      System.out.print(i + " ");
    } // 조건식이 true가 되어 continue 문이 수행되면 반복문의 끝으로 이동한다. 이 때 반복문 전체를 벗어나지는 않는다.
  }
} 

실행 결과: 1 2 4 5 7 8 10
```

반복문이 여러개로 중첩되어 있는 경우 반복문 앞에 이름을 붙이고 break 문과 continue 문에 이름을 지정해줌으로써 하나 이상의 반복문을 벗어나거나 건너뛸 수 있다.

```java
class ifContinue {
  public static void main (String[] args) {
    loop1: for(int i = 2; i <= 9; i++){
      for (int j = 1; j <= 9; j++){
        if (j == 5)
          break loop1;		//	1 ->
        // break;			//	2 ->
        // continue loop1;	//	3 ->
        // continue;		//	4 ->
        System.out.println(i + " * " + j + " = " + i * j);
      } //	-> 4
      System.out.println();	//	-> 2
    }	//	-> 3
    	//	-> 1
  }
}
```

반복문의 이름이 지정되지 않은 break 문은 자신이 속한 하나의 반복문만 벗어날 수 있으며, 반복문과 break 문에 같은 이름을 지정해주면 하나 이상의 반복문도 벗어날 수 있다. 위의 코드에서 하나씩 바꿔가며 실행시켜봄으로써 결과를 확인할 수 있다.



### Ref



