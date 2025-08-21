# 클래스

## 객체지향 프로그래밍(OOP : Object-Oriented Programming)
- 객체 지향 프로그래밍이란, 말 그대로 객체를 지향하는 프로그래밍 방법을 말한다.
- 객체란 우리 실생활에 존재하는 모든것으로 생각할 수 있다.
- 객체는 일반적으로 상태를 표현할 수 있고, 우리가 행동으로 실행할 수 있는 모든것들을 의미한다.
- 이런 객체를 중심으로 프로그램 구조를 설계하고 프로그래밍 하는 것을 객체 지향 프로그래밍이라고 한다.

### 객체란?
- 물리적으로 존재하거나 개념적인 것 중에서 다른 것과 식별 가능한 것을 말한다.
- 예를 들어 물리적으로 존재하는 자동차, 자전거, 책, 사람은 물론 개념적인 학과나 강의, 주문 등도 모두 객체가 될 수 있다.
- 객체는 속성과 동작으로 구성된다. 사람은 이름, 나이 등의 속성과 웃다, 걷다 등의 동작이 있고, 자동차는 생상, 모델명 등의 속성과 달린다, 멈춘다 등의 동작이 있다.
- 자바는 이러한 속성과 동작을 각각 ```필드(field)```와 ```메소드(method)```라고 부른다.

![image](img/객체1.png)

- 현실 세계의 객체를 소프트웨어 객체로 설계하는 것을 객체 모델링이라고 한다.
- 객체 모델링은 현실 세계 객체의 대표 속성과 동작을 추려 내어 소프트웨어 객체의 필드와 메소드로 정의하는 과정이다.
  
### 객체의 상호작용
- 현실 세계에서 일어나나 모든 현상은 객체와 객체 간의 상호작용으로 이루어져 있다.
- 예를 들어 사람은 전자계산기의 기능을 이용하고, 전자계산기는 계산 결과를 반환하는 상호작용을 한다.

	![image](img/객체상호작용.png)

### 객체간의 관계
- 객체는 단독으로 존재할 수 있지만 대부분 다른 객체와 관계를 맺고 있다.
- 관계의 종류에는 집합 관계, 사용 관계, 상속 관계가 있다.

#### 집합 관계
- 완성품과 부품관의 관계를 말한다.
- 예를 들어, 자동차는 엔진, 타이어, 핸들 등으로 구성되므로 자동차와 푸품들은 집합 관계라고 볼 수 있다.

#### 사용 관계
- 다른 객체의 필드를 읽고 변경하거나 메소드를 호출하는 관계를 말한다.
- 예를 들어 사람이 자동차에게 달린다, 멈춘다 등의 메소드를 호출하면 사람과 자동차는 사용관계라고 볼 수 있다.

#### 상속 관계
- 부모와 자식 관계를 말한다.
- 자동차가 기계의 특징(필드,메소드)을 물려받는다면 기계(부모)와 자동차(자식)는 상속 관계에 있다고 볼 수 있다.

### 객체지향 프로그래밍의 특징
#### 캡슐화
- 객체의 데이터(필드),동작(메소드)을 하나로 묶고 실제 구현 내용을 외부에 감추는 것을 말한다.
- 외부 객체는 객체 내부의 구조를 알지 못하며 객체가 노출해서 제공하는 필드와 메소드만 이용할 수 있다.

	![image](img/캡슐화.png)

- 필드와 메소드를 캡슐화 하여 보호하는 이유는 외부의 잘못된 사용으로 인해 객체가 손상되지 않도록 하는 데 있다.

#### 상속
- 객체지향 프로그래밍에서는 부모 역할의 상위 객체와 자식 역할의 하위 객체가 있다.
- 부모 객체는 자기가 가지고 있는 필드와 메소드를 자식 객체에게 물려주어 자식 객체가 사용할 수 있도록 한다.
##### 상속을 하는 이유
- 코드의 재사용성을 높여 준다.
- 유지 보수 시간을 최소화 시켜준다.

	![image](img/객체의상속.png)


#### 다형성
- 사용방법은 동일하지만 실제 결과가 다양하게 나오는 성질을 말한다.
- 자동차 부품을 교환하면 성능이 다르게 나오듯이 프로그램을 구성하는 객체(부품)를 바꾸면 프로그램의 실행 성능이 다르게 나올 수 있다.

	![image](img/객체다형성.png)

## 객체와 클래스
- 객체를 생성할 때는 설계도가 필요하다.
- 현실 세계에서 자동차를 생성하려면 자동차의 설계도가 필요하듯이, 객체지향 프로그래밍에서도 객체를 생성하려면 설계도에 해당하는 클래스가 필요하다.
- 클래스로 부터 생성된 객체를 해당 클래스의 인스턴스라고 부른다.
- 그리고 클래스로부터 객체를 만드는 과정을 인스턴스화라고 한다.
- 동일한 클래스로부터 여러 개의 인스턴스를 만들 수 있는데, 이것은 동일한 설계도로 여러 대의 자동차를 만드는것과 동일하다.

	![image](img/인스턴스화.png)

- 우리는 지금까지 많은 클래스를 선언해봤다.
- 클래스는 객체를 생성하기 위한 설계도이지만 객체를 만들지는 않았고, main()메소드만 작성해서 실행할 목적으로 클래스를 이용했다.
- 이제부터 main()메소드가 없는 클래스를 선언하고 생성해보자.

## 클래스의 선언
- 첫날부터 클래스를 만들어서 사용해왔다.
- 자바 프로그래밍의 기반이 클래스이기 때문이다.
- 우리가 사용해온 클래스의 기본 구조는 다음과 같다.

```java
접근제한자 class 클래스명{

}

접근제한자 : 클래스의 접근 범위를 제한한다.
class : class를 선언함을 뜻한다.
클래스명 : 변수처럼 이름을 가지고, 객체를 생성할 때 사용한다.
```
- 클래스는 일반적으로 하나의 소스 파일에 하나의 클래스를 선언합니다.
- 하나의 파일에서 여러개의 클래스를 선언한다면 파일이름과 같은 클래스에만 public을 사용해야 한다.

### Main01 클래스 작성
```java
package ch06.sec03;

public class SportsCar {
}

class Tire {
}
```
- 하지만 코드를 컴파일한 결과물은 코드 파일을 각각 작성한 것과 동일하게 각 class별로 도출되어 2개가 생성된다.
- 파일 분리 여부와 상관 없이 결과물이 같기 때문에, 분리 여부는 개발자가 원하는 대로 작성해도 무방하다.
- 그러나 추후 유지보수의 편리성과 클래스 재사용을 고려해 하나의 파일에 한 개의 클래스를 작성하는 것을 추천합니다.

### 클래스 이름을 작성하는 규칙
- 영어 대소문자를 사용할 수 있으며 보통 첫 글자는 대문자를 사용한다.
- 숫자를 사용할 수 있으나 첫 글자로는 사용할 수 없습니다.
- 특수문자는 $,_만 가능합니다.
- 자바 예약어(키워드)는 사용할 수 없습니다.

```java
package ch06.sec04;

public class Student {

}
```

## 객체 생성과 클래스 변수
- 클래스로부터 객체를 생성하려면 객체 생성 연산자인 new가 필요하다.
```java
new 클래스명();
```
- new 연산자 뒤에는 생성자 호출 코드가 있는데, ```클래스명()```형태를 가진다.
- new 연산자는 객체를 생성시킨 후 객체의 주소를 반환하기 때문에 클래스 변수에 다음과 같이 대입할 수 있다.

```java
클래스명 변수명 = new 클래스명();
```

```java
package ch06.sec04;

public class StudentExample {
	public static void main(String[] args) {
		Student s1 = new Student();
		System.out.println("s1 변수가 Student 객체를 참조합니다.");

		Student s2 = new Student();
		System.out.println("s2 변수가 또 다른 Student 객체를 참조합니다.");
	}
}
```

## 클래스의 종류

### 실행용 클래스 
- 프로그램 전체에서 단 하나의 클래스로, 프로그램의 실행을 맡고 있다.
- main메서드를 갖고 있으며, 다른 클래스에서 사용하지 않는다.
```java
public class Main{
	public static void main(String[] args){
		//실행하려는 코드
	}
}
```
### 객체 생성용 클래스
- 다른 클래스에서 사용할 목적으로 선언되는 클래스 입니다.
```java
public class Car{
	//속성

	//행위
}
```

```
하나의 클래스가 위 두 가지 용도의 역할을 모두 수행할 수 도 있다.
하지만 유지 보수와 객체 지향 프로그래밍의 특징인 모듈화를 고려해 별도로 분리하여 작성하는 것이 좋다.
일반적으로 하나의 프로그램에서 실행용 클래스 1개를 제외한 나머지 클래스는 모두 참조용 클래스이다.
```


## 클래스의 구성
- 클래스를 구성하는 요소는 필드,메서드, 생성자 3가지가 있다.

## 필드(field)
- 객체가 가져야할 데이터의 상태를 저장하는 변수를 말한다.
- 필드, 전역변수, 멤버 변수 라고 부르는데 다 같은말이다.
- 필드의 값을 초기화 하지 않으면 객체 생성시 자동으로 기본값으로 초기화 된다.

```java
package ch06.sec06.exam01;

public class Car {
	//필드 선언
	String model;
	boolean start;
	int speed;
}
```
- 만약 클래스를 선언할 때, 필드의 값을 초기화 하지 않으면 객체 생성 시 자동으로 기본값으로 초기화된다.
<table>
	<tr>
		<th>구분</th>
		<th>분류</th>
		<th>자료형</th>
		<th>초기값</th>
	</tr>
	<tr>
		<td rowspan="4">기본 자료형</td>
		<td>정수형</td>
		<td>byte<br>short<br>int<br>long<br></td>
		<td>0<br>0<br>0<br>0L</td>
	</tr>
	<tr>
		<td>문자형(정수)</td>
		<td>char</td>
		<td>\u0000(공백)</td>
	</tr>
	<tr>
		<td>실수형</td>
		<td>float<br>double</td>
		<td>0.0F<br>0.0</td>
	</tr>
	<tr>
		<td>논리형</td>
		<td>boolean</td>
		<td>false</td>
	</tr>
	<tr>
		<td rowspan="2" colspan="2" align="center">참조 자료형</td>
		<td>배열</td>
		<td>null</td>
	</tr>
	<tr>
		<td>클래스</td>
		<td>null</td>
</table>

- 필드는 클래스에 포함된 요소이자, 객체를 생성한 후 객체가 가지는 데이터이기도 하다.
- 따라서 객체를 생성한 후 그 객체의 필드를 사용할 수 있다.
```java
객체명.필드명

객체명 : 클래스를 이용해 만든 객체의 이름
필드명 : 만든 객체가 가지고 있는 필드의 이름
```
```java
package ch06.sec06.exam01;

public class CarExample {
	public static void main(String[] args) {
		//Car 객체 생성
		Car myCar = new Car();

		//Car 객체의 필드값 읽기
		System.out.println("모델명: " + myCar.model);
		System.out.println("시동여부: " + myCar.start);
		System.out.println("현재속도: " + myCar.speed);
	}
}
```

### 필드의 사용
- 필드를 사용한다는 것은 필드값을 읽고 변경하는 것을 말한다.
- 클래스에서 필드를 선언했다고 해서 바로 사용할 수 있는 것은 아니다.
- 필드는 객체의 데이터이므로 객체가 존재하지 않으면 필드도 존재하지 않는다.
- 클래스로부터 객체가 생성된 후에 필드를 사용할 수 있다.
- 필드는 객체 내부의 생성자와 메소드 내부에서 사용할 수 있고, 객체 외부에서도 접근해서 사용할 수 있다.

```java
package ch06.sec06.exam02;

public class Car {
	//필드 선언
	String company = "현대자동차";
	String model = "그랜저";
	String color = "검정";
	int maxSpeed = 350;
	int speed;
}
```
```java
package ch06.sec06.exam02;

public class CarExample {
	public static void main(String[] args) {
		//Car 객체 생성
		Car myCar = new Car();

		//Car 객체의 필드값 읽기
		System.out.println("제작회사: " + myCar.company);
		System.out.println("모델명: " + myCar.model);
		System.out.println("색깔: " + myCar.color);
		System.out.println("최고속도: " + myCar.maxSpeed);
		System.out.println("현재속도: " + myCar.speed);

		//Car 객체의 필드값 변경
		myCar.speed = 60;
		System.out.println("수정된 속도: " + myCar.speed);
	}
}
```

# 생성자

## 생성자의 선언과 호출
- 클래스를 구성하는 구성요소중 하나인 생성자는, 객체를 생성할 때 호출되어 객체의 초기화를 담당하는 특별한 메서드이다.
- 객체를 생성하고 초기화하기 위해서는 반드시 생성자를 호출해야 한다.

```java
클래스명 변수명 = new 클래스명();
				    ---------
						↓
					생성자의 호출

```

- 생성자가 성곡적으로 실행이 끝나면 new 연산자는 객체의 주소를 반환한다.
- 반환된 주소는 클래스 변수에 대입되어 객체의 필드나 메소드에 접근할 때 이용된다.

## 기본생성자
- 자바의 모든 클래스에는 ```하나 이상의 생성자가 정의```되어야 있어야 한다.
- 클래스를 생성하면서 개발자가 직접 생성자를 선언하지 않았지만, 자바 컴파일러가 다음과 같은 기본생성자를 자동으로 제공해주고 있다.
```java
public 클래스명() { }
```
- 다만, 컴파일러의 눈에만 보일 뿐 우리가 보는 코드에는 생략되어 있다.
- 클래스가 public class로 선언되면 기본 생성자도 public이 붙지만, 클래스가 public없이 class로만 선언되면 기본 생성자에도 public이 붙지 않는다.
- 예를 들어 Car클래스를 설계할 때 생성자를 생략하면 기본생성자가 다음과 같이 생성된다.
```java
public class Car{

}

↓ 컴파일

public class Car{

	public Car(){ //자동 추가

	}
}
```
- 그렇기 때문에 다음과 같이 new 연산자 뒤에 기본 생성자를 호출할 수 있다.
```java
Car myCar = new Car();
				------
					↓ 
				기본 생성자의 호출
```


## 생성자 선언
- 객체를 다양하게 초기화하기 위해 개발자는 생성자를 다음과 같이 직접 선언할 수 있다.
```java
접근제어자 클래스명 (매개변수1,매개변수2...){
	//객체의 초기화 코드
}
```
- 생성자는 반환값이 없지만, 반환 타입을 아예 작성하지 않는다.(void로도 적지 않는다.)
- 매개변수는 new 연산자로 생성자를 호출할 때 매개값을 생성자 블록 내부로 전달하는 역할을 한다.
- 예를 들어 다음과 같이 Car 생성자를 호출할 때 3개의 매개값을 블록 내부로 전달한다고 가정해보자.
```java
Car myCar = new Car("그랜저","검정",300);
```
- 3개의 매개값을 순서대로 매개변수로 대입받기 위해서는 다음과 같이 생성자가 선언되어야 한다.
```java
public class Car{
	//생성자 선언
	Car(String model, String color, int maxSpeed){
		...
	}
}
```
- 매개변수의 타입은 매개값의 종류에 맞게 작성하면 된다.
```java
package ch06.sec07.exam01;

public class Car {
	//생성자 선언
	Car(String model, String color, int maxSpeed) {
	}
}
```
```java
package ch06.sec07.exam01;

public class CarExample {
	public static void main(String[] args) {
		Car myCar = new Car("그랜저", "검정", 250);
		//Car myCar = new Car();  //기본 생성자 호출 못함
	}
}
```

## 필드 초기화
- 객체마다 동일한 값을 갖고 있다면 필드 선언 시 초기값을 대입하는 것이 좋고, 객체마다 다른 값을 가져야 한다면 생성자에서 필드를 초기화 하는 것이 좋다.
- 예를 들어 Korean 클래스를 선언한다고 가정해보자.
- 한국인이므로 nation(국가)은 대한민국으로 동일한 값을 갖지만, name(이름)과ssn(주민등록번호)은 한국인마다 다르므로 생성자에서 초기화 하는것이 좋다.
```java
package ch06.sec07.exam02;

public class Korean {
	//필드 선언
	String nation = "대한민국";
	String name;
	String ssn;

	//생성자 선언
	public Korean(String n, String s) {
	  name = n;
	  ssn = s;
	}
}
```
- 생성자의 매개변수에 들어가는 값은 생성자를 호출할 때 주어진다.
```java
package ch06.sec07.exam02;

public class KoreanExample {
	public static void main(String[] args) {
		//Korean 객체 생성
		Korean k1 = new Korean("박자바", "011225-1234567");
		//Korean 객체 데이터 읽기
		System.out.println("k1.nation : " + k1.nation);
		System.out.println("k1.name : " + k1.name);
		System.out.println("k1.ssn : " + k1.ssn);
		System.out.println();

		//또 다른 Korean 객체 생성
		Korean k2 = new Korean("김자바", "930525-0654321");
		//또 다른 Korean 객체 데이터 읽기
		System.out.println("k2.nation : " + k2.nation);
		System.out.println("k2.name : " + k2.name);
		System.out.println("k2.ssn : " + k2.ssn);
	}
}
```
- 위 예제의 Korean 생성자를 보면 매개변수 이름으로 각 n과 s를 사용했다.
- 매개변수의 이름이 너무 짧으면 가독성이 좋지 않기 때문에 가능하면 초기화시킬 필드명과 동일한 이름을 사용하는 것이 좋다.
```java
package ch06.sec07.exam03;

public class Korean {
	// 필드 선언
	String nation = "대한민국";
	String name;
	String ssn;

	// 생성자 선언
	public Korean(String name, String ssn) {
		this.name = name;
		this.ssn = ssn;
	}
}
```
- 매개변수명이 필드명과 동일하기 때문에 필드임을 구분하기 위해 this키워드를 필드명 앞에 붙여 주었다.
- this는 현재 객체를 말하며, this.name은 현재 객체의데이터(필드)로서의 name을 뜻한다.

## Person 클래스
```java
public class Person {
	int age;
	String name;

	//예를들어서 나이와 이름, 전화번호를 알아야 친구가 된다고 가정을 해볼게요.
	//이중에 한가지라도 빼먹고 안쓰면 문제가 있는거에요 써먹기 불가능한 객체가 될수도 있다는거죠.

	//똑같은걸 계속 만드려고 한다면 기본생성자에 값을 넣어놓는것도 좋은 방법
	//pbulic Person() {
	//	age = 40;
	//	name = "노태문";
	//}

	//빈공간에서 cntl + space bar 기본생성자 생성
	//임의로 새로운 생성자를 정의한 순간부터 기본생성자는 쓸 수 없다.
	public Person(int age, String) {
		this.age = age;
		this.name = name;

	}

	public void introduce() {
		System.out.printf("안녕하세요. 저는 %d살 %s입니다.", age,name);
	}
}
```
## PMain 클래스
```java
public class PMain{
	public static void main(String[] args) {
		
		Person p1 = new Person(20,"홍길동");
		Person p2 = new Person(30,"김자바");

		p1.introduce();
		p2.introduce();
		
}
```

## 생성자 오버로딩
- 매개값으로 객체의 필드를 다양하게 초기화하려면 생성자 오버로딩이 필요하다.
- 생성자 오버로딩이란 매개변수를 달리하는 생성자를 여러 개 선언하는 것을 말한다.

### 오버로딩 규칙
1. 매개변수의 개수가 다를 때
2. 매개변수의 개수가 같아도 자료형이 다를 때
3. 생성자나 메서드의 이름은 그대로 사용해야 한다.

```java
public class Car{
	Car(){ ... }
	Car(String model){ ... }
	Car(String model, String color) { ... }
	Car(String model, String color, int maxSpeed) { ... }
}
```
- 매개변수의 타입과 개수 그리고 선언된 순서가 똑같을 경우 매개변수 이름만 바꾸는 것은 생성자 오버로딩이 아니다.
```java
Car(String model, String color) { ... }
Car(String color, String model) { ... } //오버로딩이 아님 컴파일 에러 발생
```

```java
package ch06.sec07.exam04;

public class Car {
	//필드 선언
	String company = "현대자동차";
	String model;
	String color;
	int maxSpeed;
	
	//생성자 선언
	Car() {}
	
	Car(String model) { 
		this.model = model; 
	}
	
	Car(String model, String color) {
		this.model = model;
		this.color = color;
	}
	
	Car(String model, String color, int maxSpeed) {
		this.model = model;
		this.color = color;
		this.maxSpeed = maxSpeed;
	}
}
```
```java
package ch06.sec07.exam04;

public class CarExample {
	public static void main(String[] args) {
		Car car1 = new Car();
		System.out.println("car1.company : " + car1.company);
		System.out.println();

		Car car2 = new Car("자가용");
		System.out.println("car2.company : " + car2.company);
		System.out.println("car2.model : " + car2.model);
		System.out.println();
		
		Car car3 = new Car("자가용", "빨강");
		System.out.println("car3.company : " + car3.company);
		System.out.println("car3.model : " + car3.model);
		System.out.println("car3.color : " + car3.color);
		System.out.println();
		
		Car car4 = new Car("택시", "검정", 200);
		System.out.println("car4.company : " + car4.company);
		System.out.println("car4.model : " + car4.model);
		System.out.println("car4.color : " + car4.color);
		System.out.println("car4.maxSpeed : " + car4.maxSpeed);
	}
}
```
### 다른 생성자 호출
- 생성자 오버로딩이 많아질 경우 생성자 간의 중복된 코드가 발생할 수 있다.
- 매개변수의 수만 달리하고 필드 초기화 내용이 비슷한 생성자에서 이러한 중복 코드를 많이 볼 수 있다.
```java
Car(String model){
	this.model = model;
	this.color = "은색";
	this.maxSpeed = 250;
}

Car(String model, String color){
	this.model = model;
	this.color = color;
	this.maxSpeed = 250;
}

Car(String model, String color, int maxSpeed){
	this.model = model;
	this.color = color;
	this.maxSpeed = maxSpeed;
}
```
- 이 경우에는 공통 코드를 한 생성자에만 집중적으로 작성하고, 나머지 생성자는 this(...)를 사용하여 공통 코드를 가지고 있는 생성자를 호출하는 방법으로 개선할 수 있다.
```java
Car(String model){
	this(model,"은색",250);
}

Car(String model, String color){
	this(model,color,250);
}

Car(String model, String color, int maxSpeed){
	this.model = model;
	this.color = color;
	this.maxSpeed = maxSpeed;
}
```
```java
package ch06.sec07.exam05;

public class Car {
	// 필드 선언
	String company = "현대자동차";
	String model;
	String color;
	int maxSpeed;
	
	Car(String model) {
		//20라인 생성자 호출
		this(model, "은색", 250);
	}

	Car(String model, String color) {
		//20라인 생성자 호출
		this(model, color, 250);
	}

	Car(String model, String color, int maxSpeed) {
		this.model = model;
		this.color = color;
		this.maxSpeed = maxSpeed;
	}
}

package ch06.sec07.exam05;

public class CarExample {
	public static void main(String[] args) {
		Car car1 = new Car("자가용");
		System.out.println("car1.company : " + car1.company);
		System.out.println("car1.model : " + car1.model);
		System.out.println();

		Car car2 = new Car("자가용", "빨강");
		System.out.println("car2.company : " + car2.company);
		System.out.println("car2.model : " + car2.model);
		System.out.println("car2.color : " + car2.color);
		System.out.println();
		
		Car car3 = new Car("택시", "검정", 200);
		System.out.println("car3.company : " + car3.company);
		System.out.println("car3.model : " + car3.model);
		System.out.println("car3.color : " + car3.color);
		System.out.println("car3.maxSpeed : " + car3.maxSpeed);
	}
}
```

# 메서드

## 메서드 선언과 호출
- 메소드 선언은 객체의 동작을 실행하는 블록으로 정의하는 것을 말하고, 메소드 호출은 실행 블록을 실제로 실행하는 것을 말한다.
- 메소드는 객체 내부에서도 호출되지만 다른 객체에서도 호출될 수 있기 때문에 객체 간의 상호작용 방법을 정의하는 것이라고 볼 수 있다.

### 메서드 선언
- 메서드는 크게 선언부(signature)와 실제 영역(body)로 구성되어 있다.
```java
접근 제한자 반환타입 메서드명(){
	//기능을 수행하는 코드
}
```
#### 반환타입(return Type)
- 메서드를 호출하면 메서드는 블록 안에 있는 코드들을 실행한 후 결과값을 반환한다.
- 이때 결과값을 어떤타입으로 반환할것인지 미리 정해주는것이다.
- 반환값이 없는 경우 타입으로 'void'를 쓰면 된다.
```java
void powerOn() { ... } //리턴값이 없는 메소드 선언
double divide(int x, int y) { ... } //double 타입 값을 리턴하는 메소드 선언
```

#### 메서드명(함수명)
- 메서드명은 말그대로 메서드의 이름(첫글자는 소문자로 시작한다.)
- 메서드를 호출할 때 사용한다.
```java
void run() { ... }
void setSpeed(int speed) { ... }
String getName() { ... }
```

#### 매개변수
- 메소드를 호출할 때 전달한 매개값을 받기 위해 사용된다.
- 다음 예에서 divide() 메소드는 연산할 두 수를 전달받아야 하므로 매개변수가 2개 필요하다.
- 전달할 매개값이 없다면 매개변수는 생략할 수 있다.

```java
double divide(int x, int y) { ... }
```
- 매개변수는 '매개변수의 자료형'과'매개 변수명'으로 선언할 수 있다.
```java
				  int number;
전달받을 값의 자료형 ┘ 	  └ 메서드 안에서 사용할 이름

```
#### 실행블록
- 메소드 호출 시 실행되는 부분이다.
```java
package ch06.sec08.exam01;

public class Calculator {
	//리턴값이 없는 메소드 선언
	void powerOn() {
		System.out.println("전원을 켭니다.");
	}

	//리턴값이 없는 메소드 선언
	void powerOff() {
		System.out.println("전원을 끕니다.");
	}

	//호출 시 두 정수 값을 전달받고,
	//호출한 곳으로 결과값 int를 리턴하는 메소드 선언
	int plus(int x, int y) {
		int result = x + y;
		return result; //리턴값 지정;
	}

	//호출 시 두 정수 값을 전달받고,
	//호출한 곳으로 결과값 double을 리턴하는 메소드 선언
	double divide(int x, int y) {
		double result = (double)x / (double)y;
		return result; //리턴값 지정;
	}
}
```
### 메소드의 호출
- 메소드를 호출한다는 것은 <b style="color:red">메소드 블록을 실행</b>하는 것을 말한다.
- 클래스에서 메소드를 선언했다고해서 바로 호출할 수 있는 것은 아니다.
- 메소드는 객체의 동작이므로 <b style="color:red">객체가 존재하지 않으면 메소드를 호출할 수 없다.</b>
- 클래스로부터 객체가 생성된 후에 <b style="color:red">메소드는 생성자와 다른 메소드 내부에서 호출될 수 있고, 객체 외부에서도 호출될 수 있다.</b>
- 객체 내부에서는 단훈시 메소드명으로 호출하면 되지만, 외부 객체에서는 참조 변수와 도트( . )연산자를 이용해서 호출한다.
- 또한 메소드가 매개변수를 가지고 있을 때는 호출할 때 매개변수의 타입과 수에 맞게 매개값을 제공해야 한다.
- 메소드가 리턴값이 있을 경우에는 대입 연산자를 사용해서 다음과 같이 리턴값을 변수에 저장할 수 있다.

	<br>

	```java
	타입 변수 = 메소드();
	```
	<br>

```java
package ch06.sec08.exam01;

public class CalculatorExample {
	public static void main(String[] args) {
		//Calculator 객체 생성
		Calculator myCalc = new Calculator();
		
		//리턴값이 없는 powerOn() 메소드 호출
		myCalc.powerOn();

		//plus 메소드 호출 시 5와 6을 매개값으로 제공하고,
		//덧셈 결과를 리턴 받아 result1 변수에 대입
		int result1 = myCalc.plus(5, 6);
		System.out.println("result1: " + result1);

		int x = 10;
		int y = 4;
		//divide() 메소드 호출 시 변수 x와 y의 값을 매개값으로 제공하고,
		//나눗셈 결과를 리턴 받아 result2 변수에 대입
		double result2 = myCalc.divide(x, y);
		System.out.println("result2: " + result2);

		//리턴값이 없는 powerOff() 메소드 호출
		myCalc.powerOff();
	}
}
```
### 가변길이 매개변수
- 메소드를 호출할 때에는 매개변수의 개수에 맞게 매개값을 제공해야 한다.
- 만약 메소드가 가변길이 매개변수를 가지고 있다면 매개변수의 개수와 상관없이 매개값을 줄 수 있다.
- 가변길이 매개변수는 다음과 같이 선언한다.
```java
int sum(int ... values){

}
```
- 가변 길이 매개변수는 메소드 호출 시 매개값을 쉼표로 구분해서 개수와 상관없이 제공할 수 있다.
```java
int result = sum(1,2,3);
int result = sum(1,2,3,4,5);
```
- 매개값들은 자동으로 배열 항목으로 변환되어 메소드에서 사용된다.
```java	
int[] values = {1,2,3};		
int result = sum(values);

int result = sum(new int[] {1,2,3});
```

<br>

```java
package ch06.sec08.exam02;

public class Computer {
	//가변길이 매개변수를 갖는 메소드 선언
	int sum(int ... values) {
		//sum 변수 선언
		int sum = 0;
		
		//values는 배열 타입의 변수처럼 사용
		for (int i = 0; i < values.length; i++) {
			sum += values[i];
		}

		//합산 결과를 리턴
		return sum;
	}
}

package ch06.sec08.exam02;

public class ComputerExample {
	public static void main(String[] args) {
		//Computer 객체 생성
		Computer myCom = new Computer();

		//sum() 메소드 호출 시 매개값 1, 2, 3을 제공하고
		//합산 결과를 리턴 받아 result1 변수에 대입
		int result1 = myCom.sum(1, 2, 3);
		System.out.println("result1: " + result1);

		//sum() 메소드 호출 시 매개값 1, 2, 3, 4, 5를 제공하고
		//합산 결과를 리턴 받아 result2 변수에 대입
		int result2 = myCom.sum(1, 2, 3, 4, 5);
		System.out.println("result2: " + result2);

		//sum() 메소드 호출 시 배열을 제공하고
		//합산 결과를 리턴 받아 result3 변수에 대입
		int[] values = { 1, 2, 3, 4, 5 };
		int result3 = myCom.sum(values);
		System.out.println("result3: " + result3);

		//sum() 메소드 호출 시 배열을 제공하고
		//합산 결과를 리턴 받아 result4 변수에 대입
		int result4 = myCom.sum(new int[] { 1, 2, 3, 4, 5 });
		System.out.println("result4: " + result4);
	}
}
```

### return
- return 문은 메소드의 실행을 강제 종료하고 호출한 곳으로 돌아간다는 의미이다.
- 메소드 선언에 반환타입이 있을 경우에는 return문 뒤에 리턴값을 추가로 지정해야 한다.

```java
접근제한자 반환타입 메서드명(){
	//기능을 수행할 코드들
	...
	return 리턴값;
}
```
- return 문 이후에 실행문을 작성하면 'Unreachable code'라는 컴파일 에러가 발생한다.
- 왜냐하면 return문 이후의 실행문은 결코 실행되지 않기 때문이다.
```java
int plus(int x, int y){
	int result = x + y;
	return result;
	//System.out.println(result) Unreachable code
}
```
- 하지만 다음과 같은 경우에는 컴파일 에러가 발생하지 않는다.
```java
boolean isLeftGas(){
	if(gas == 0){
		System.out.println("gas가 없습니다."); // 1
		return false;
	}
	System.out.println("gas가 있습니다."); // 2
	return true;
}
```
- if 문의 조건식이 false가 되면 정상적으로 2가 실행되기 때문에 2는 'Unreachable code'에러를 발생시키지 않는다.
- if문의 조건식이 true가 되면 1이 실행되고 return false가 실행되어 메소드는 즉시 종료되므로 당연히 2는 실행되지 않는다.

<br>

```java
package ch06.sec08.exam03;

public class Car {
	//필드 선언
	int gas;

	//리턴값이 없는 메소드로 매개값을 받아서 gas 필드값을 변경
	void setGas(int gas) {
		this.gas = gas;
	}

	//리턴값이 boolean인 메소드로 gas 필드값이 0이면 false를, 0이 아니면 true를 리턴
	boolean isLeftGas() {
		if (gas == 0) {
			System.out.println("gas가 없습니다.");
			return false; // false를 리턴하고 메소드 종료
		}
		System.out.println("gas가 있습니다.");
		return true; // true를 리턴하고 메소드 종료
	}

	//리턴값이 없는 메소드로 gas 필드값이 0이면 return 문으로 메소드를 종료
	void run() {
		while (true) {
			if (gas > 0) {
				System.out.println("달립니다.(gas잔량:" + gas + ")");
				gas -= 1;
			} else {
				System.out.println("멈춥니다.(gas잔량:" + gas + ")");
				return; // 메소드 종료
			}
		}
	}
}
```
<br>

```java
package ch06.sec08.exam03;

public class CarExample {
	public static void main(String[] args) {
		//Car 객체 생성
		Car myCar = new Car();

		//리턴값이 없는 setGas() 메소드 호출
		myCar.setGas(5);

		//isLeftGas() 메소드를 호출해서 받은 리턴값이 true일 경우 if 블록 실행
		if(myCar.isLeftGas()) {
			System.out.println("출발합니다.");
			
			//리턴값이 없는 run() 메소드 호출
			myCar.run();
		}
		
		System.out.println("gas를 주입하세요.");
	}
}
```

### 메소드 오버로딩
- 생성자 오버로딩과 같이 매개변수의 타입, 개수, 순서가 다른 메소드를 여러 개 선언하는 것을 말한다.
```
class 클래스 {
	리턴 타입	메소드명	(타입 변수, ...) {...}
		↕		↕			↕
	  무관		동일		타입,개수,순서가 다른 메소드를 여러개 선언
		↕		↕			↕
	리턴 타입	메소드명	(타입 변수, ...) {...}
}
```
- 메소드 오버로딩의 목적은 다양한 매개값을 처리하기 위해서이다.
- 다음 예에서 plus() 메소드는 두 개의 int 타입 매개값만 처리하고 double 타입 매개 값은 처리할 수 없다.
```java
int plus(int x, int y){
	int result = x + y;
	return result;
}
```
- 만약 double 타입 값도 처리하고 싶다면 다음과 같이 plus()메소드를 오버로딩하면 된다.
```java
int plus(double x, double y){
	double result = x + y;
	return result;
}
```
- 메소드 오버로딩의 대표적인 예는 콘솔에 출력하는 System.out.println()메소드로, 호출할 때 주어진 매개값의 타입에 따라서 오버로딩된 println() 메소드 중 하나를 실행한다.

```java
void println() { ... }
void println(double x) { ... }
void println(int x) { ... }
void println(String x) { ... }
```

<br>

```java
package ch06.sec08.exam04;

public class Calculator {
	//정사각형의 넓이
	double areaRectangle(double width) {
		return width * width;
	}
	
	//직사각형의 넓이
	double areaRectangle(double width, double height) {
		return width * height;
	}
}
```
<br>

```java
package ch06.sec08.exam04;

public class CalculatorExample {
	public static void main(String[] args) {
		//객체 생성
		Calculator myCalcu = new Calculator();

		//정사각형의 넓이 구하기
		double result1 = myCalcu.areaRectangle(10);
		
		//직사각형의 넓이 구하기
		double result2 = myCalcu.areaRectangle(10, 20);

		System.out.println("정사각형 넓이=" + result1);
		System.out.println("직사각형 넓이=" + result2);
	}
}
```

# this와 this()
- 변수명을 지을 때, 최대한 구체적이고 명확하게 작명하는 것이 보다 효율적인 코드를 작성하는데 도움이 된다는 것을 알고있다.
- 함수나 생성자에서 매개변수는 클래스의 필드보다 우선순위가 높아서, 대입연산자를 기준으로 왼쪽/오른쪽 변수 모두 매개변수를 뜻하게 된다.
- 매개변수에 매개변수를 넣는 의미없는 코드가 된다.
- 이러한 상황을 해결하기 위해 this키워드를 사용한다.

## this
- 객체 자기 자신 스스로 참조
- this 참조 변수는 객체가 자기 자신을 참조하는데 사용하는 변수이다.
- this를 필드에 붙여서 사용하면, 중괄호{}안에서도 같은 이름의 매개변수와 필드를 구분해서 사용할 수 있다.
```java
this.필드 = 매개변수명;
```

### Student.java
```java
package test3;

public class Student {
	String name;
	int age;
	int studentID;
	
	public Student(String name, int age, int studentID) {
		this.name = name;
		this.age = age;
		this.studentID = studentID;
	}
}

```

## this()
- 현재 클래스에 선언되어있는 생성자를 가리킬 수 있는 키워드이다.

### this(매개변수1,매개변수2)
- this()메서드는 같은 클래스 안에 있는 생성자 중 매개변수의 개수, 자료형, 순서에 맞는 다른 생성자를 호출하는 메서드로 생성자 내부에서만 사용할 수 있다.

### Phone.java
```java
package test3;

public class Phone {
	String brand;
	int series;
	String color = "검정색";

	public Phone(String b, int s) {
		brand = b;
		series = s;
	}

	public Phone(String b, int s, String c) {
		//brand = b;
		//series = s;
		this(b,s); //this()는 첫줄에서만 사용할 수 있다.
		color = c;
	}

	public void phoneInfo() {
		System.out.println(color + " " + brand + " " + series);
	}
}
```


## 정적 멤버와 static
- 클래스 안에서 선언된 필드와 메서드를 클래스 멤버라고도 부른다.
- 클래스에 포함된 요소라는 의미로 '멤버'라는 용어를 사용한다.
#### 모든 객체가 동일한 값을 가져야할 때 각 객체의 멤버로 만들어야 할까???

### Family클래스 생성하기
```java
package member;

public class Family { //클래스 선언
	String name; //구성원 이름
	int age; //구성원 나이
	String address = "서울";//구성원 주소
}
```

### FamilyMain클래스 생성하기
```java
package member;

public class FamilyMain {
	public static void main(String[] args) {
		Family father = new Family();
		Family son = new Family();
		
		father.address = "인천";
		System.out.println(son.address);
	}
}
결과 : 서울
```
- 같은 집으로 함께 이사를 한 가족이라도 하나의 객체의 주소만 변경했더니 아들 객체의 주소는 바뀌지 않은 것을 알 수 있다.
- 모든 객체의 필드 값이 같아야 한다면 매우 불편한 상황이 될 수 있다.
- 일반적으로 각 객체가 가지게 되는 필드와 메서드를 인스턴스 멤버 라고 한다.
- 모든 객체들이 공유하며 사용하는 하나의 필드와 메서드를 정적 멤버라고 부른다.

### 정적 멤버
- 필드와 메서드를 선언할 때 static이라는 키워드가 붙은 멤버를 말한다.


### static키워드
- 사전적으로 '고정된'이라는 뜻을 가지고 있다.
- 프로그래밍 언어에서 static은 '클래스에 고정되었다'라는 의미로 사용되고 있다.
- 쉽게 말해서 객체가 아닌 클래스에 의존적인 요소라고 생각하면 된다.
- 멤버 앞에 static 키워드를 붙히게 되면, 다른 멤버들과 달리 객체를 생성하지 않고 바로 사용할 수 있다.
- **그 이유는 객체를 생성할 때 메모리에 올라가는 것이 아니라, 프로그램이 실행될 때 메모리에 올라가고 프로그램이 종료될 때 메모리에서 사라지기 때문이다.**

### 호출방법
```
클래스명.필드;
클래스명.메서드명();
```

### Student클래스 생성하기
```java
package member;

public class Student {
	static String schoolName = "코리아 고등학교"; //정적 멤버 선언
	
	static void goToSchool() {
		System.out.println("학교에 갑니다");
	}
}
```

### StudentMain클래스 생성하기
```java
package test2;

public class StudentMain {
	public static void main(String[] args) {
		System.out.println(Student.schoolName);
		Student.goToSchool();
	}
}
결과
코리아 고등학교
학교에 갑니다.
```
- 정적 멤버의 경우, 객체마다 가지는 데이터 기능이 아니기 때문에 모든 객체가 같은 값을 가져야 할 경우에 사용하는 것이 효율적이다.
- 따라서 각 클래스의 멤버를 선언할 때는 충분히 고려한 후 정적 멤버로 선언할지에 대한 결정을 내리는 것이 좋다.

### Student클래스에 코드 추가하기
```java
package test2;

public class Student {//클래스 선언
	static String schoolName = "코리아 고등학교";//정적 필드 선
	String studentName; //인스턴스 필드 선
	
	static void goToSchool() { //정적 메서드 선언
		System.out.println("학교에 갑니다.");
	}
	
	void hello() { //인스턴스 메서드 선언
		System.out.println("안녕하세요, 제 이름은 " + studentName + "입니다.");
	}
}
```

### StudentMain클래스에 코드 추가하기
```java
package test2;

public class StudentMain {
	public static void main(String[] args) {
		Student stu1 = new Student();
		stu1.studentName = "김고이";
		stu1.hello();
		System.out.println("학교는 " + Student.schoolName + "입니다.");
		Student.goToSchool();
		System.out.println("----------------------");
		Student stu2 = new Student();
		stu2.studentName = "김고";
		stu2.hello();
		System.out.println("학교는 " + Student.schoolName + "입니다.");
		Student.goToSchool();
	}
}
결과
안녕하세요, 제 이름은 김고이입니다.
학교는 코리아 고등학교입니다.
학교에 갑니다.
----------------------
안녕하세요, 제 이름은 김고입니다.
학교는 코리아 고등학교입니다.
학교에 갑니다.
```
- 정적 멤버를 호출할 때, 객체 변수를 통해 호출할수도 있습니다.
```
Student stu1 = new Student();
System.out.println(stu1.schoolName);
```



## 메서드 사용의 이점
- 메서드를 구현함으로써, 같은 내용의 코드를 반복적으로 사용하는 것을 피할 수 있다. 
- 반복되는 문장들을 묶어서 메서드로 작성해놓으면 필요할 때마다 재사용이 가능하기 때문이다.
- 코드의 집합을 따로 분리하는것을 "모듈화"라고 한다.
- 모듈화를 하면 코드를 읽을 때 가독성이 좋아지며, 프로그램을 수정할 때 더욱 빠르고 쉽게 할 수 있다.



### 접근제한자
- 접근제한자는 클래스/메서드/필드에 대한 접근을 어디범위까지 제한하느냐에 대한 지시어이다.
1. public : 모든 접근을 허용. 같은 프로젝트 내의 모든 객체들이 사용할 수 있도록 허용.
2. private : 현재 클래스 내에서만 사용을 허가.
3. protected : 상속관계의 객체들에만 사용을 허가.
4. default : 같은 패키지(폴더)내의 객체에만 사용을 허가(아무것도 쓰지 않으면 default)




### Method01클래스 생성
```java
package method;

public class Method01 {
	public static void main(String[] args) {
		printHello(); //main메서드 안에서 printHello()메서드 호
	}
	
	static void printHello() {
		System.out.println("안녕하세요");
		System.out.println("만나서 반갑습니다.");
	}
}
```
- main메서드도 static으로 프로그램 시작과 함께 메모리에 올라가 있다.
- 따라서 main안에서 메서드를 호출하기 위해서는 호출하는 메서드가 메모리에 올라가 있어야 한다.

### 메서드를 메모리에 올리는 두 가지 방법
- 객체 생성용 클래스에 있는 경우
  - 인스턴스 메서드 : 객체를 생성함과 동시에 객체의 멤버들이 메모리에 올라간다. 따라서 객체를 생성한 후 사용할 수 있다.
  - 정적 메서드 : 프로그램 시작과 동시에 메모리에 자동으로 올라가기 때문에 바로 사용할 수 있다.
- 실행용 클래스에 있는 경우
  - 객체를 생성할 방법이 없기 때문에, 메서드가 무조건 static으로 선언되어야 한다.

## 메서드의 호출
- 메서드는 다른 메서드에서 호출되어 사용된다.
```
클래스명 변수명 = new 클래스명(); -> 객체를 생성하여 변수에 담기
변수명.메서드명();
```

- 메서드는 클래스 안에서 선언되므로 메서드를 사용하기 위해서는 해당 클래스의 객체부터 생성해야 한다.

### Jogger클래스 생성하기
```java
package method;

public class Jogger {

	void run() {
		System.out.println("run run run!!");
	}
}
```

### JoggerMain클래스 생성하기
```java
package method;

public class JoggerMain {
	public static void main(String[] args) {
		Jogger jogger = new Jogger(); //객체 생성
		jogger.run(); //jogger인스턴스의 run()메서드 호출
	}
}
결과
run run run!!
```
### 2개 이상의 메서드 선언하기
- 메서드는 같은 클래스에 있는 필드를 사용할 수 있다.
- 하나의 클래스에 2개 이상의 메서드를 사용하는 것 역시 가능하다.
### Jogger클래스에 코드 추가힉
```java
package method;

public class Jogger {

	String name; //조거의 이름
	
	void run() {
		System.out.println("run run run!!");
	}
	
	void sayName() {
		System.out.println("제 이름은 : " + name + "입니다.");
	}
}
```
### JoggerMain에 코드 추가하기
```java
package method;

public class JoggerMain {
	public static void main(String[] args) {
		Jogger jogger = new Jogger(); //객체 생성
		jogger.name = "김나비";
		jogger.sayName();
		jogger.run(); //jogger인스턴스의 run()메서드 호출
	}
}
결과
제 이름은 : 김나비입니다.
run run run!!
```

### Book클래스 생성하기
```java
package test3;

public class Book {
	public void count(int bookNum) {
		System.out.println("책은 " + bookNum+"권 입니다.");
	}
}
```
### BookMain클래스 생성하기
```java
package test3;

public class BookMain {
	public static void main(String[] args) {
		Book myBook = new Book(); //객체 생성
		myBook.count(3); //myBook 인스턴스 count메서드 호출
	}
}
```
- 파라미터의 개수에는 제한이 없다.
- 2개 이상의 파라미터를 정의할 때는 콤마(,)를 기준으로 변수를 여러개 만들면 된다.
```java
접근제한자 반환형 메서드명(자료형 변수명1,자료형 변수명2...){

}
```
### Calc클래스 생성하기
```java
package method;

public class Calc {

	void sum(int num1, int num2) {
		System.out.println("두 수의 합은 : " + (num1 + num2) + "입니다.");
	}
}
```

### CalcMain클래스 생성하기
```java
package method;

public class CalcMain {
	public static void main(String[] args) {
		Calc calc = new Calc();
		calc.sum(5, 3);
		calc.sum(10, 7);
	}
}
```
- 다른 자료형 2개를 매개변수로 받는 메서드

### Person클래스 생성하기
```java
package method;

public class Person {
	void introduce(String name, int age) {
		System.out.println("제 이름은 " + name+"이고, 나이는" + age+"세입니다.");
	}
	
	void hello() {
		System.out.println("안녕하세요");
	}
}
```

### PersonMain클래스 생성하기
```java
package method;

public class PersonMain {
	public static void main(String[] args) {
		Person hong = new Person();
		hong.introduce("홍길동", 20);
		hong.hello();
	}
}
결과
제 이름은 홍길동이고, 나이는20세입니다.
안녕하세요
```
- 배열을 매개변수로 받는 메서드

### Calc클래스에 코드 추가하기
```java
package method;

public class Calc {

	void sum(int num1, int num2) {
		System.out.println("두 수의 합은 : " + (num1 + num2) + "입니다.");
	}
	
	void sum(int[] nums) {
		int result = 0;
		for(int i = 0; i < nums.length; i++) {
			result += nums[i];
		}
		System.out.println("숫자들의 합은 : " + result + "입니다.");
	}
}
```

### CalcMain클래스에 코드 추가하기
```java
package method;

public class CalcMain {
	public static void main(String[] args) {
		Calc calc = new Calc();
		calc.sum(5, 3);
		calc.sum(10, 7);
		
		int []nums = {100,200};
		calc.sum(nums);
	}
}
```



### Calc클래스 수정하기
```java
package method;

public class Calc {

	void sum(int num1, int num2) {
		System.out.println("두 수의 합은 : " + (num1 + num2) + "입니다.");
	}
	
	//반환값의 타입과 일치시켜준다.
	int sum(int[] nums) {
		int result = 0;
		for(int i = 0; i < nums.length; i++) {
			result += nums[i];
		}
		//System.out.println("숫자들의 합은 : " + result + "입니다.");

		return result; //모든 기능을 수행한 값을 반환한다.
	}
}
```

### CalcMain클래스 수정하기
```java
package method;

public class CalcMain {
	public static void main(String[] args) {
		Calc calc = new Calc();
		calc.sum(5, 3);
		calc.sum(10, 7);
		
		int []nums = {100,200};
		//calc.sum(nums);
		System.out.println("숫자들의 합은 " + calc.sum(nums)+"입니다.");
	}
}
```
- 메서드를 호출한 위치가 메서드를 실행하고 반환된 결과값으로 치환되었다.
- 변수에 저장하지 않고 바로 치환하여 사용할 수도 있으며, 필요에 따라 저장하여 결과값을 활용할 수도 있다.

### 반환받은 값을 변수에 저장하는 메서드
### MidTerm클래스 생성하기
```java
package method;

public class MidTerm {
	public int score(int[] scores) {
		int result = 0;
		for(int i = 0; i < scores.length; i++) {
			result += scores[i];
		}
		return result;
	}
}
```

### MidTermMain클래스 생성하기
```java
package method;

public class MidTermMain {
	public static void main(String[] args) {
		int [] studentA = {97,53};
		int [] studentB = {97,66};
		
		MidTerm mid = new MidTerm(); //MidTerm 객체 생성
		int sumA = mid.score(studentA); //메서드를 호출한 결과값을 sumA에 저장
		int sumB = mid.score(studentB); //메서드를 호출한 결과값을 sumB에 저장
		
		if(sumA > sumB) {
			System.out.println("A학생의 중간고사 총점이 더 높습니다.");
		} else if(sumA < sumB) {
			System.out.println("B학생의 중간고사 총점이 더 높습니다.");
		} else {
			System.out.println("두 학생의 중간고사 총점이 같습니다.");
		}
	}
}
```
### 메서드를 빠져나가기 위한 return
#### Bus클래스
```java
package test3;

public class Buss {

	public void take(int m) {
		while(true) {
			if(m < 3000) {
				System.out.println("교통카드를 충전하러 갑니다.");
				return;
			}
			System.out.println("버스를 탑니다.");
			m-=1250;
		}
	}
}
```
#### BusMain클래스
```java
package test3;

public class BusMain {

	public static void main(String[] args) {
		int money = 10000;
		Bus bus = new Bus();
		bus.take(money);
	}
}
```

## 클래스의 로딩
- 자바의 클래스들이 언제 어디서 메모리에 올라가고 클래스 멤버들이 초기화 되는 방법

### JVM의 클래스 로더(class Loader)
- 클래스 로더는 컴파일된 자바의 클래스파일(.class)을 동적으로 로드한다.
- JVM의 메모리 영역인 데이터 영역에 배치하는 작업을 수행한다.
- class파일을 로딩하는 순서
    1. Loading(로드):클래스 파일을 가져와서 JVM의 메모리에 로드한다.
    2. Linking(링크) : 클래스 파일을 사용하기 위해 검증하는 과정
    3. Initializtion(초기화) : 클래스 변수들을 적절한 값으로 초기화 한다.
- 유의할 점은 Loading 기능은 한번에 메모리에 올리지 않고, 어플리케이션에서 필요한 경우 동적으로 메모리에 적재하게 된다는 점이다.
- 곰곰히 생각해보면 언제 어디서 사용될지 모르는 static 멤버들을 처음에 전부 메모리에 올린다는건 비효율적이다.
- JVM은 실행될때 모든 클래스를 메모리에 올려놓지 않고, 그때 마다 필요한 클래스를 메모리에 올려 효율적으로 관리하는 것이다.

# setter&getter
- 지금까지 객체의 필드를 객체의 내부뿐만 아니라 객체 밖에서도 마음껏 사용할 수 있었고, 마음대로 값을 바꿀수도 있었다.
## 필드에 직접 접근했을 때의 문제점
### Person클래스 수정하기
```java
package method;

public class Person {
//	void introduce(String name, int age) {
//		System.out.println("제 이름은 " + name+"이고, 나이는" + age+"세입니다.");
//	}
//	
//	void hello() {
//		System.out.println("안녕하세요");
//	}
	
	int age;
}
```

### PersonMain클래스 수정하기
```java
package method;

public class PersonMain {
	public static void main(String[] args) {
		Person hong = new Person();
//		hong.introduce("홍길동", 20);
//		hong.hello();
		hong.age = -30;
		
		System.out.println("hong의 나이는 " + hong.age+"세입니다.");
	}
}
```
- 사람의 나이는 음수가 될 수 없음에도 age값을 음수로 바꿀 수 있었다.
- 이처럼 객체 밖에서 필드에 마음대로 접근할 수 있고 값을 변경할 수 있다면, 문제가 생길 가능성이 있다.
- 이런 문제를 예방하기 위해 객체 지향 프로그래밍에서는 메서드를 통해서 필드의 값을 불러오고, 필드의 값을 변경하는 방법을 이용한다.

### 메서드를 통해 필드에 접근할 때 장점
- 필드를 보호할 수 있다.
- 메서드에서 필드에 들어갈 값을 검증한 후 필드에 대입할 수 있다.
- 외부에서 사용할 필드의 값을 정제한 후 값을 제공할 수 있다.

## setter
- 외부에서 메서드를 통해 데이터에 접근하고 검증할 수 있도록 유도하는 메서드의 개념

### Person클래스에 코드 추가하기
```java
public void setAge(int num) {
	if(num <= 0) {// 만약, age에 넣으려는 값이 0보다 작거나 같다면
		System.out.println("잘못된 수를 입력하셨습니다. 1 이상의 값으로 설정하세요");
		return; //메서드 종료
	} else {
		age = num; //age필드에 num을 저장
	}
}
```
- 일반적으로 setter메서드를 사용할 때는, 필드의 값을 객체 외부에서 직접 넣지 못하도록 필드에 접근을 제한한다.
- 필드가 선언되어 있는 클래스에서만 접근이 가능하도록 private 접근제한자를 붙힌다.
```java
private int age;
```
- 필드를 private으로 선언함으로써 필드를 한층 더 보호할 수 있으나, 객체의 외부에서 그 필드에 대한 값을 불러오는 것 또한 불가능해졌다.

## getter
- private 필드를 객체 외부에서 값을 불러오기 위해 구현하는 메서드를 getter라고한다.
- private 필드는 객체 외부에서는 접근이 불가능하지만, 필드가 선언된 클래스에서는 어디서든 접근이 가능하다.
- 따라서 메서드를 통해서 값을 전달해 줄 수 있다.

### Person클래스에 코드 추가하기
```java
public int getAge() {
	return age;
}
```

### PersonMaim클래스 코드 수정하기
```java
package method;

public class PersonMain {
	public static void main(String[] args) {
		Person hong = new Person();
//		hong.introduce("홍길동", 20);
//		hong.hello();
		//hong.age = -30;
		hong.setAge(-30);
		hong.setAge(30);
		System.out.println("hong의 나이는 " + hong.getAge()+"세입니다.");
	}
}
```

## setter&getter 실습
```java
package test3;

public class Car {
	//필드(인스턴스 변수, 객체 변수, 멤버 변수)
	private int speed;
	private boolean stop;
	
	public int getSpeed() {
		return speed;
	}
	
	public void setSpeed(int speed) {
		if(speed < 0) {
			this.speed = 0;
			return;
		} else {
			this.speed = speed;
		}
		
	}
	
	public boolean isStop() {
		return stop;
	}
	
	public void setStop(boolean stop) {
		this.stop = stop;
		this.speed = 0;
	}
}
```
```java
package test3;

public class CarTest {
	public static void main(String[] args) {
		Car myCar = new Car();
		
		//잘못된 속도 변경
		myCar.setSpeed(-50);
		
		System.out.println("현재 속도 : " + myCar.getSpeed());
		
		//올바른 속도 변경
		myCar.setSpeed(60);
		
		//멈춤
		if(!myCar.isStop()) {
			myCar.setStop(true);
		}
		
		System.out.println("현재 속도 : " + myCar.getSpeed());
	}
}

```
