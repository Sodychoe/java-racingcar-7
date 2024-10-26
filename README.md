# 자동차 경주 게임 기능 명세서

## ✅ 애플리케이션 기능 명세

### 자동차 이름 입력받기

- [ ] 사용자에게 자동차 이름을 입력하라는 메시지를 출력한다
- [ ] 사용자로부터 쉼표로 구분된 자동차의 이름들을 입력받는다

### 시도 횟수 입력받기

- [ ] 사용자에게 시도 횟수를 입력하라는 메시지를 출력한다
- [ ] 사용자로부터 시도 횟수 문자열을 입력받는다

### 자동자 경주 진행하기

- [ ] 사용자에게 입력받은 시도 횟수만큼 차수를 반복한다
- [ ] 각 진행 차수에서, 자동차가 전진하려고 할 때 0 이상 9 이하의 정수값을 생성하고, 그 값이 4 이상이면 자동차가 전진한다
- [ ] 한 번의 차수가 종료되면 자동차들의 전진 거리를 이름과 함께 출력한다

### 우승자 결정하기

- [ ] 모든 차수가 종료되면 전진한 거리가 가장 큰 자동차를 우승자로 결정한다
- [ ] 자동차 경주는 1명 이상의 우승자를 가질 수 있다
- [ ] 우승자를 결정 후 그 결과를 출력한다

### 애플리케이션 실행 결과 예시

```
경주할 자동차
이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi :-
woni :
jun :-

pobi :--
woni :-
jun :--

pobi :---
woni :--
jun :---

pobi :----
woni :---
jun :----

pobi :-----
woni :----
jun :-----

최종 우승자 :pobi,jun
```

## ⚠️ 예외처리

사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException` 을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 자동차 이름 입력 예외처리

- [ ] 이름이 비어있는 경우
- [ ] 이름에 공백만 있는 경우
- [ ] 이름이 5자를 초과하는 경우
- [ ] 입력한 이름이 중복되는 경우

### 시도 횟수 입력 예외처리

- [ ] 시도 횟수가 숫자가 아닌 경우
- [ ] 시도 횟수가 정수가 아닌 경우
- [ ] 시도 횟수가 0 이하인 경우

## 💯 테스트 완료 여부

### 기능 테스트

| 구분              | 테스트 항목       | 구현 | 단위 테스트 | 
|-----------------|--------------|:--:|:------:|
| **자동차 이름 입력**   | 입력 메시지 출력    | ✅  |   ✅    | 
|                 | 자동차 이름 입력 받기 | ✅  |   ✅    |
| **경주 시도 횟수 입력** | 입력 메시지 출력    | ⬜  |   ⬜    |
|                 | 시도 횟수 입력 받기  | ⬜  |   ⬜    |  
| **자동차 경주 진행**   | 자동차 전진 시도    | ✅  |   ✅    |  
|                 | 차수별 위치 상태 출력 | ⬜  |   ⬜    |  
|                 | 최종 우승자 선정    | ⬜  |   ⬜    |  
|                 | 최종 우승자 출력    | ⬜  |   ⬜    | 

### 예외 처리 테스트

| 구분         | 예외 상황     | 예외 처리                                                 | 구현 | 테스트 |
|------------|-----------|-------------------------------------------------------|:--:|:---:|
| **자동차 이름** | 빈 이름 입력   | IllegalArgumentException("자동차 이름은 비워둘 수 없습니다.")       | ⬜  |  ⬜  |
|            | 공백 이름     | IllegalArgumentException("자동차 이름은 공백일 수 없습니다.")       | ⬜  |  ⬜  |
|            | 이름 5자 초과  | IllegalArgumentException("자동차 이름은 5자 이하여야 합니다.")      | ⬜  |  ⬜  |
|            | 중복된 이름    | IllegalArgumentException("자동차 이름은 서로 중복될 수 없습니다.")    | ⬜  |  ⬜  |
| **시도 횟수**  | 숫자가 아닌 입력 | IllegalArgumentException("시도할 횟수에 숫자가 아닌 값이 입력되었습니다") | ⬜  |  ⬜  |
|            | 정수가 아닌 숫자 | IllegalArgumentException("시도할 횟수는 정수여야 합니다.")         | ⬜  |  ⬜  |
|            | 0 이하의 숫자  | IllegalArgumentException("시도할 횟수는 0 이상이어야 합니다.")      | ⬜  |  ⬜  |




