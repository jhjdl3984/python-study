# 문제 제목: 영수증

## 문제 정보
- **출처:**  백준
- **난이도:** Easy, Medium, Hard 중 하나.

## 문제 설명
구매한 물건의 가격과 개수로 계산한 총 금액이 영수증에 적힌 총 금액과 일치하는지 검사

X = 구매 총 금액
N = 구매한 물건의 종류의 수
a = 각 물건의 가격
b = 각 물건의 개수

## 해결 과정
X와 N을 따로 입력 받고, a와 b를 입력받아 각 물건의 금액을 total에 순차적으로 더한다.
total이 구매 총 금액과 같다면 Yes를 반환, 같지 않다면 No를 반환

### 접근 방법
for문으로 total에 순차적으로 값을 더해서 if문으로 같은지 구별한다.

## 코드
```python
X = int(input())
N = int(input())

# a, b = map(int, input().split())
total = 0

    for i in range(N):
        a, b = map(int, input().split())
        total += (a * b)

    if total == X:
        return 'Yes'
    else:
        return 'No'
