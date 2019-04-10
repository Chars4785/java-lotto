# Java Lotto
![lottoExample](./src/img/lottoExample.png)

- 적은 금액에 해당하는 로또를 산다.
- 지난 주 당첨 번호를 적는다.
- 당첨된 금액과 수익률을 출력해준다.

## 1. 기능 구현

- 로또 금액 관련 기능

    - 로또 구입 금액을 입력 받는 기능
    - 금액이 1000원 아래, 10만원 초과인 경우 예외 처리
    - 숫자가 아닌 다른 값, 음수인 값일 경우 예외 처리

- 로또 구입 관련 기능

    - 가격에 맞는 로또 구입 및 출력 기능
    - 로또를 사고 남은 거스름돈 처리 예외
    - 번호가 (1~45까지) 생성이 제대로 안될 경우의 예외 처리
    - 번호가 중복 안되게 생성

- 번호 입력 관련 기능

    - 지난주 당첨 번호 6개, 보너스 볼 1개 입력 받는 기능
    - 총 7개의 숫자보다 많은 숫자 또는 숫자가 아닌 값을 입력시 예외 처리
    - 7개의 숫자가 중복되는지 확인 하는 기능
    - 1~45까지 숫자인지 확인

- 당첨 통계 관련 기능

    - 당첨된 금액과 나머지 출력
    - 수익률 소수점 3자리까지 계산해 출력해야 한다.
    - 손해 여부 판단하는 기능

## 4. 클래스
<pre>
    LottoGame : 게임을 하는 플레이 하는 main 공간을 의미하는 객체
    Controller : 게임의 흐름을 컨트럴하는 마스터 객체
    Lotto : 로또 한장을 의미하는 객체
    Rank : 로또 등수를 의미하는 enum
    WinningLotto : 당첨 번호를 담당하는 객체
</pre>

## 5. 메소드
- LottoGame

- Controller
    - Controller : 생성자
    - askHowMuch : 로또 구입을 얼마나 할지 물어보는 기능
    - isNumber : 구입으로 적은 금액이 숫자인지 판단하는 기능
    - checkInputRangeRight : 입력받은 금액이 한도 금액에 맞는지 판단하는 기능
    - buyLotto : 입력된 금액 만큼 로또를 구매
    - calculateLottoAmount : 몇개의 로또와 거스름돈이 생기는지 출력하는 기능
    - makeRandomNumber : 7개의 숫자 생성
    - checkNumberToList : 숫자가 7개 생성되는지, 중복이 없는지 체크하는 기능
    - showLottosNumber : 산 로또의 모든 숫자 출력하는 기능
- Lotto
    - getNumbersList : 각 로또가 갖고 있는 번호 반환
- Rank
- WinningLotto
