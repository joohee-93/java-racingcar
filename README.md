# 자동차 경주 게임

# 자동차 경주 프로세스

## 순서

1. 자동차 이름을 입력받는다.
2. 경기 시도 횟수를 입력받는다.
3. 자동차 객체를 입력받은 이름 갯수만큼 초기화 한다.
   - 자동차 객체는 자신의 이름과 위치 값을 갖는다.
4. 입력받은 경기 횟수 만큼 경기를 반복한다.
   - 각 자동차 객체는 0~9 까지 무작위 값을 추첨하여 4이상인 경우 위치 값을 1증가 (전진) 시키고, 4미만인 경우 전진하지 않는다.
5. 원하는 시점에 자동차의 현재 상태를 화면에 출력한다.
6. 경기가 끝나면 위치 값을 비교하여 우승자를 출력한다. (단, 같은 값인 경우 공동 우승처리 한다.)

# 기능 목록

## 객체

### 자동차 객체(Car)
  - [x] 이름(name)
  - [x] 위치 값(position)
  - [x] 전진 함수(forward)
    - 자동차의 위치 값을 증가 시키는 함수
  - [x] 현재 상태 출력 함수(showPosition)
    - 현재 자동차의 상태 (위치값) 을 출력하는 함수
  - [x] 자동차의 현재 위치가 인수의 값보다 앞인지 판단하는 함수(isAheadOf)
  - [x] 자동차의 현재 위치가 인수의 값과 같은지 판단(isEqualOf)

### 레이싱 관련 함수 제공 객체(RacingHost)
  - [x] 경주를 위한 자동차 객체 생성 및 자동차 저장 객체 리턴 함수(initCar)
    - 사용자의 입력 값을 추출해 이름을 가져오고, 개수만큼 자동차를 생성하고, 자동차를 저장한 객체를 리턴.
  - [x] 값 입력 함수(inputString)
    - 사용자의 입력 값을 받아 저장하는 함수
  - [x] 경주 1회 수행 함수(racing)
    - 경주 1회를 수행
  - [x] 무작위 값 추첨 함수(draw)
    - 0~9 사이 값을 추첨하는 함수
  - [x] 우승자 계산 및 출력 함수(chooseWinner)
    - 현재 자동차들의 위치값을 비교하여 최대값을 계산 후, 우승자를 결정 및 출력하는 함수
  - [x] 자동차 이름에 대한 예외처리 함수(carNameValidChk)

