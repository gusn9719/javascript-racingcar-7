# javascript-racingcar-precourse

## 구현할 기능 목록

1. 입력 기능
   - 사용자의 입력을 통해 경주에 참가할 자동차 이름과 시도할 횟수를 입력받습니다.
      - `경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)` 
         - 예시 입력 : `pobi,woni , jun`
         - 자동차 이름은 5자 이하로 제한 되며, 앞뒤 공백이 제거됩니다.
         - 길이가 0인 이름은 입력 될 수 없습니다.
      - `시도할 횟수는 몇 회인가요?`
         - 예시 입력 : `5`
         - 시도 횟수는 1 이상의 양수여야 합니다.
      - 잘못된 입력 시 `[ERROR]`로 시작하는 오류 메시지를 출력하고 프로그램을 종료합니다.

2. 자동차 전진 기능
   - 각 자동차는 주어진 시도 횟수만큼 전진하거나 멈추는 과정을 반복합니다.
      - 전진 조건 : 0에서 9사이의 랜덤 숫자를 생성하여, 숫자가 4 이상일 경우 자동차가 전진합니다.
      - 전진 여부는 `Random.pickNumberInRange(0,9)`를 이용하여 결정합니다.

3. 경주 진행 및 결과 출력 기능
   - 각 시도마다 모든 자동차의 위치를 출력합니다.
      - 출력 예시 : 
         실행 결과
         pobi : -
         woni : -
         jun : 
   - 각 라운드마다 경주 결과를 모두 출력합니다.

4. 우승자 출력 기능
   - 모든 시도가 완료된 후 가장 멀리 전진한 자동차를 우승자로 선정합니다.
      - 우승자가 여러 명일 경우 쉼표`(,)`로 구분하여 출력합니다.
      - 예시 출력 : 최종 우승자 : pobi, jun

5. 테스트 케이스 작성
   - 모든 기능 구현 후, Jest를 이용하여 테스트 코드를 작성합니다.
      - 입력 값 검증 테스트 : 자동차 이름이 올바른지, 시도 횟수가 유효한지를 검증
      - 파라미터화 테스트 : 다양한 입력 조합에 대해 반복 테스트하기 위해 `test.each()` 또는 `descibe.each()` 를 사용