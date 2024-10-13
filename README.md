# 기본 계산기 및 공학 계산기

이 저장소는 두 개의 Python 클래스를 포함하고 있습니다: `Calculator`와 `EngineeringCalculator`. `Calculator` 클래스는 기본적인 사칙연산 기능을 제공하며, `EngineeringCalculator`는 더 발전된 로그, 삼각 함수, 거듭제곱 계산 등을 추가로 제공합니다.

## 주요 기능

### 기본 계산기 (`Calculator` 클래스)
- **더하기 (`add`)**: 여러 숫자를 더합니다.
- **빼기 (`subtract`)**: 첫 번째 숫자에서 나머지 숫자들을 뺍니다.
- **곱하기 (`multiply`)**: 여러 숫자를 곱합니다.
- **나누기 (`divide`)**: 첫 번째 숫자를 나머지 숫자로 나눕니다. 0으로 나눌 때 예외 처리.
- 소수점 자리수를 지정하거나 결과를 `float` 타입으로 변환하는 기능 지원.

### 공학 계산기 (`EngineeringCalculator` 클래스)
- `Calculator` 클래스를 상속받아 추가적인 공학 관련 기능을 제공합니다:
  - **제곱근 (`square_root`)**: 숫자의 제곱근을 계산합니다.
  - **거듭제곱 (`power`)**: 숫자의 거듭제곱을 계산합니다.
  - **로그 (`log`)**: 주어진 숫자의 로그를 계산합니다 (기본 베이스는 10).
  - **자연로그 (`ln`)**: 자연 로그(베이스 `e`)를 계산합니다.
  - **사인 (`sin`)**: 각도의 사인 값을 계산합니다 (라디안 또는 도 단위).
  - **코사인 (`cos`)**: 각도의 코사인 값을 계산합니다 (라디안 또는 도 단위).
  - **탄젠트 (`tan`)**: 각도의 탄젠트 값을 계산합니다 (라디안 또는 도 단위).
- 소수점 자리수, `float` 타입으로 결과 반환, 각도 단위 지정 (라디안 또는 도) 기능을 지원.

## 설치 방법

추가적인 외부 의존성은 필요하지 않으며, 계산기는 Python의 내장 모듈인 `math`만 사용합니다. 저장소를 복제하거나 다운로드하여 사용하세요.

```bash
git clone https://github.com/your-repository/calculator.git
cd calculator
```

## 사용 예시
Calculator 및 EngineeringCalculator 클래스는 아래와 같이 사용할 수 있습니다:

```python
from calculator import Calculator, EngineeringCalculator

# 기본 계산기 예시
calc = Calculator(precision=2, return_float=True)
reault1 = calc.add(10, 5.1264, 3, precision=2, return_float=True) 
reault2 = calc.subtract(10, 5.1264, 3, precision=2, return_float=True)
reault3 = calc.multiply(10.1234, 5.5678, precision=2, return_float=True)
reault4 = calc.divide(100.1234, 5.5678, precision=2, return_float=True)

print(result1)  # 결과 : 18.13
print(result2)  # 결과 : 1.87
print(result3)  # 결과 : 56.34
print(result4)  # 결과 : 17.98


# 공학 계산기 예시
eng_calc = EngineeringCalculator()
result5 = eng_calc.power(2, 3)
result6 = eng_calc.log(8, base=2)
result7 = eng_calc.ln(1)
result8 = eng_calc.sin(30)
result9 = eng_calc.cos(60)
result10 = eng_calc.tan(45)

print(result5)  # 결과 : 8.0
print(result6)  # 결과 : 3.0
print(result7)  # 결과 : 0.0
print(result8)  # 결과 : 0.5
print(result9)  # 결과 : 0.5
print(result10)  # 결과 : 1.0
```
소수점 자릿수를 지정하거나 결과값을 float으로 반환하도록 설정할 수 있습니다. 예를 들어, 삼각 함수의 경우 각도를 도(degree) 또는 라디안(radian) 단위로 지정할 수 있습니다.

## 라이선스
이 프로젝트는 MIT 라이선스에 따라 사용 가능합니다.

