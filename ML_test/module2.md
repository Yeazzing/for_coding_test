# Module 2 – Data Manipulation:
- 목표: 데이터 조작을 위한 기본적인 코딩 기술을 평가한다.
- 구성: 1개의 기본 코딩 질문으로, 평균 10-15분 소요되며 15-20라인의 코드가 예상된다.
포함 내용: 숫자(기본 연산, 자릿수 분리), 문자열(splitting, comparing, modifying, concatenating, reversing), 배열(iterating, modifying, reversing)과 같은 기본 데이터 구조(data structure) 개념의 3-5가지 조합. 주로 한두 개의 중첩 루프(nested loops)로 해결 가능한 요구사항과 명확한 구현 단계(implementation steps)를 가진 설명이 포함된다.
- 제외 내용: 패턴 인식이나 증명이 필요한 내용, 알고리즘 최적화(optimizing algorithms)가 필요한 내용, 고전적 또는 틈새 알고리즘(classic or niche algorithms)에 대한 지식이 필요한 내용.

---
## 기본 개념

### Numbers: Digit Manipulation (숫자 및 자릿수 처리)

- 숫자를 다룰 때는 단순히 계산하는 것을 넘어 각 자릿수를 분리하거나 특정 조건으로 필터링하는 능력을 요구
- 핵심 기법: 숫자를 문자열로 변환하여 처리하거나, 산술 연산(%와 //)을 사용해 자릿수를 추출합니다.
- 예시 상황: 숫자 리스트가 주어졌을 때, 각 숫자의 자릿수 합이 짝수인 경우만 추출하기
- 자릿수 분리 예시

```
num = 123
digit_sum = sum(int(d) for d in str(num)) # 문자열 변환 활용
# 또는 산술 연산 활용
# while num > 0: digit_sum += num % 10; num //= 10
```

### Strings: Transformation & Comparison (문자열 변형 및 비교)

- 문자열 파트는 쪼개기(Splitting), 뒤집기(Reversing), 수정(Modifying) 등의 작업을 3~5가지 섞어서 출제
- 핵심 기법: split()으로 단어를 나누고, 슬라이싱([::-1])으로 뒤집거나, join()으로 다시 합치는 과정이 필수
- 예시 상황: 문장 내 단어들을 분리한 뒤, 각 단어의 첫 글자와 마지막 글자를 서로 바꾸고 다시 공백으로 합치기
- 문자열 수정 예시

```
word = "Code"
# 파이썬 문자열은 불변(Immutable)이므로 리스트로 변환하여 수정
chars = list(word)
chars[0], chars[-1] = chars[-1], chars[0]
new_word = "".join(chars)
```

### Arrays: Iteration & Conditional Logic (배열 순회 및 조건 로직)

- 배열은 보통 중첩 루프(Nested loops)를 사용해 요소를 수정하거나 새로운 배열을 생성하는 문제가 나옵니다.
- 핵심 기법: 특정 조건을 만족하는 요소만 골라내어 새 배열을 만들고, 그 배열의 순서를 뒤집거나 다른 배열의 앞에 붙이는(Appending) 작업
- 예시 상황: 배열에서 홀수와 짝수를 각각 다른 리스트에 담은 뒤, 짝수 리스트를 뒤집어서 홀수 리스트 앞에 붙이기
- 배열 조작 예시 (조건부 분리 및 합치기)

```python
arr = [1, 2, 3, 4, 5]
evens = [x for x in arr if x % 2 == 0]
odds = [x for x in arr if x % 2 != 0]
result = evens[::-1] + odds # 짝수 뒤집어 홀수 앞에 붙이기
```
