# .md 파일 작성 법
"#" 제일 큰 제목
> 구글링 참조.
">" 약간 흐릿한 주석



* "*" 은 동그라미로 바뀝니다
  * "*" 밑의 "*" 은 하위 말머리 입니다.




### Compiled

* 컴파일이 필요하다.
* 컴파일러가 필요하다.
* 컴파일 하는 시점이 있다.(컴파일 타임)
* 컴파일된 결과물을 실행한다.
* 컴파일된 결과물을 실행하는 시점이 있다.



### Interpreted

* 컴파일이 필요없다.
* 컴파일러가 필요없다.
* 컴파일하는 시점이 없다.
* 코드 자체를 실행한다.
* 코드를 실행하는 시점이 있다.(런타임)



### Traditional Compiled Language

* 컴파일 언어라고 한다.
* C, C++, Go, C#, Java, ...
* 프로그래머가 작성한 **소스코드**를 기계어로 변환하는 과정을 **컴파일**이라고 한다.
* 기계어로 변환된 결과물을 **Object Code(목적 코드)**라 한다.
* **컴파일**하는 프로그램을 **컴파일러**라고 한다.
* **컴파일**하는 동안을 **Compile Time** 이라고 한다.
* 컴파일된 코드는 프로세서에 따라 다르다
* 소스 코드에서는 OS 에 따라 라이브러리가 다르다.
* 컴파일된 코드는 작은 크기에 최적화 된다.
* 일반적으로 실행시 기계어로 바꾸는(인터프리터 언어)보다 빠르다.
  * 실행시 기계어로 바꿔주는 연산이 필요없기 때문이다.
* 컴파일된 코드들은 **Linking**이라는 과정을 통해 실행 파일로 만들어 진다.
  * 컴파일된 여러 목적 코드들을 합치고 라이브러리를 추가한다.
  * Linking하는 프로그램을 Linker라고 한다.
  * 컴파일이라는 말을 링킹까지 포함하여 말하기도 한다.



**타입스크립트는 링킹과정이 없다.**



### 결론적으로

* 우리는 타입스크립트의 문법을 알아야 하고,
* 타입스크립트가 자바스크립트로 변환되는 컴파일 과정에서
* 컴파일러의 옵션을 통해 어떻게 제어할 수 있는지,
* 컴파일을 도와주는 역할을 하는 어떤 기구들이 있는지를 학습하는 것이 목표다. 
