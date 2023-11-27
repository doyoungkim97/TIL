# Java Collection - 1
> 해당 블로그 자료는 남궁성 님의 JAVA 의 정식 3rd 를 학습하고 정리한 기록 글입니다.
자료의 원본 및 출처는 [남궁성님의 자바의 정석 github](https://github.com/castello/javajungsuk_basic/tree/master)

## JAVA 컬렉션
컬렉션 프레임워크는 다수의 데이터를 다루는데 필요한 다양하고 풍부한 클래스들을 제공하기 위해서 사용된다.
**인터페이스 다형성**을 제공하기 때문에 객체지향석 설계를 통해 표준화 되어있어 재사용성이 뛰어남

컬렉션 프레임워크에는 크게 3가지의 인터페이스가 정의
각 List, Set, Map 이 있고 List와 Set은 Collection에서 각각 상속받은 자식 클래스이다.

- **List**
순서가 있는 데이터 집합, 중복 허용
ex) ArrayList, LinkedList, Stack, Vector
- **Set**
순서를 유지 X, 데이터 중복 허용 X
ex) HashSet, TreeSet
- **Map**
key, value의 쌍으로 이루어진 데이터 집합
순서 유지 X, 키를 중복 허용 X, 값 중복 허용 O
ex) HaspMap, TreeMap ...

여기서 Vector, Hashtable은 기존 컬레션 클래스는 호환을 위해서 유지, 실제로는 사용 지양

## Collection 인터페이스
컬렉션의 메소드는 다음과 같다
아래 메소드 표처럼 객체를 추가, 삭제, 확인 하는 여러 메소드가 있다.
여기에 Lambda, Stream 기능도 있지만 추후 자료에서 설명예정 💨
![](https://velog.velcdn.com/images/kimdodo/post/ffa18ff5-adf8-4664-b1de-4d8b7f2bbb8f/image.png)

## List 인터페이스
파이썬에서도 List를 정말 많이 사용했고 C#에서도 나는 많이 사용했다.
특히 C++에서 없는 Slice 기능들이 정말 좋았는데 Java에서 어떠할까
Vector도 있지만 가장 흔하게 사용하는건 ArrayList, LinkedList, Stack 정도

상속받은 Collection 기능은 제외하고 기록
이전에 모 부트캠프에서 List로 저장된 객체에 int 배열을 변화해서 저장하려고 하는데 그 방법을 몰라서 못했던 기억이 있다.
아래 메소드를 잘 기억하고 체득하는게 중요
![](https://velog.velcdn.com/images/kimdodo/post/fcbffd96-05e8-47ec-88ab-dccf2375b68e/image.png)

## Set인터페이스
중복을 허용하지 않고 순서가 없는 자료형
해당 기능도 파이썬에서 있었다. Set을 통해서 중복 제거 하고 관계대수의 Union같은 기능 썼음

## Map
key,value로 구성된 쌍으로 묶인 컬렉션 클래스
HashMap,LinkedHashMap 등이 있음
아래는 각 메소드
values()의 반환 타입이 Collection, keySet()에서 반환타입이 Set인것에 주목
즉 Key는 중복이 없기 때문에 Set으로 반환되고 values를 중복을 허용하고 순서가 없기 때문에 컬렉션으로 반환된다.

![](https://velog.velcdn.com/images/kimdodo/post/b658b07e-1d11-4e87-beeb-de956b8ab4ae/image.png)

> **✅ Map.Entry 인터페이스**
Map 인터페이스의 내부 인터페이스
Map에 저장되는 Key-Value 쌍을 다루기 위해 내부적으로 Entry 인터페이스를 정의
해당 사항은 추가예시로 설명예정

이제 컬렉션이 무엇이 이고 어떤 인터페이스 지원하는지 알았다.
내부적으로 각 3개의 인터페이스에서 각각 어떤 세부 자료구조를 구현하는지 다음강의에서 알아보자

