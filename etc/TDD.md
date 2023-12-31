# TDD

배민 출신 이동욱님의 책을 읽고, 유튜브 내용을 보면 TDD를 정말 많이 강조하신다.
우테코 프리코스에서도 TDD를 많이 언급하는 것으로 보아 배민에서는 TDD를 중요하게 생각한다고 볼 수 있다.
빅테크 기업에서 강조하는 TDD는 무엇일까??

## TDD(Test Driven Development)
TDD란 테스트 주도 개발의 약자이다.
반복테스트를 이용한 소프트웨어 방법론
작은 단위로 테스트 케이스를 작성하고 이를 통과하는 코들르 추가하는 단계를 반복하여 구현한다.

TDD의 실횽성을 업무로 경험한 사람들은 효과적인 TDD를 실무에 적용하기 위해서 노력하지만
각 환경마다의 편차가 존재한다.

## TDD 개발주기
![](https://velog.velcdn.com/images/kimdodo/post/b2942a60-5bdc-472c-aab9-3cce4dd93625/image.png)

🟥Red 에서는 실패하는 테스트 코드를 먼저 작성한다.
🟩Green에서는 테스크 코드를 성공시키기 위한 실제 코드를 작성한다.
🟦Blue에서는 중복 코드 제거, 일반화를 통한 리팩토링을 수행한다.

여기서 중요한 것은 실패하는 테스트 코드를 작성할 때 까지 실제 코드를 작성하지 않는것과 실패하는 테스트를 통과할 정도의 최소 실제 코드를 작성해야하는 것이다.

아래 그림을 통해서 상세하게 보자
실제 코드에 기대되는 바를 명확하게 정의하고 불필요한 설계를 피하며 정확한 요구 사항에 집중가능

![](https://velog.velcdn.com/images/kimdodo/post/bb6243c5-267f-4fb5-9c6d-41d274c8016c/image.png)

간단한 예시로 이해해보자

> 문제 : 생년월일을 입력받으면 나이를 출력하는 프로그램

> 1. 처음에는 간단한 것을 목표( 태어난 해와 올해 연도를 입력해서 연도 뺄셈으로 나이 계산
2015,2018 ====> 만 3살
2. 만들기 전에 만든 후에 무엇을 테스트 할지 설계 (실패 테스트)
2015,2018을 입력하면 2가 나오는 테스트 프로그램을 생성
3.가 다음에 그 테스트를 통과할 프로그램 생성
2018-2015(올해 년도- 입력 연도)
4. 테스트 프로그램으로 이 프로그램 실행
5. 통과시 새로운 테스트를 추가
생월을 추가했을때 계산하는 프로그램

이 1-5 과정을 반복수행한다.

솔직히 이렇게만 이해하면 왜 이렇게 해야하는지를 이해하기가 어렵다
그렇기 떄문에 추가 설명을 통해서 다시 알아볼 예정이다.