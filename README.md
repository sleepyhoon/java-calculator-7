# 우아한테크코스 프리코스 1주차

# 문자열 덧셈 계산기

## 기능 명세서

### 1. 문자열을 입력받는다.

사용자로부터 문자열을 입력받는다.

### 2. 문자열을 파싱하여 커스텀 구분자가 있으면 식별한다.

입력받은 문자열에서 커스텀 구분자가 있다면 이를 식별한다. 커스텀 구분자는 따로 배열에 보관한다.

### 3. 덧셈 연산을 진행한다.

구분자를 기준으로 분리한 각 숫자의 합을 반환한다. 매우 큰 수도 더할 수 있게 `BigInteger`을 사용한다.

### 4. 잘못된 입력에 대한 에러 반환

위 과정에서 잘못된 입력을 받은 경우 `IllegalArgumentException` 예외를 발생시킨다.
아래 과정을 모두 만족해야 에러가 발생하지 않는다.

1. 구분자 입력이 유효한가? (// + 구분자 + \n)
    1. 여기서 유효한가? 라는 질문은 구분자를 받을 때 **"시작은 '//' 으로 시작하고, 끝날 때는 '\n' 으로 끝나는가?" 이다.**
2. 입력한 문자열이 구분자 배열 내에 선언된 구분자로 구분되었는가?
3. 입력된 정수가 양수인가?
4. 아무것도 입력하지 않으면 0을 출력하는가?