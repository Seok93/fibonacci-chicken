#나무위키 알고리즘 정리
피보나치수열 예시: 1 1 2 3 5 8 13 21 ...
입력: 사람 인원 수 N(임의의 자연수) 출력: 치킨마리수 N

문제 분할:
1. 임의의 자연수 N에 대해 제켄도르프의 정리를 이용하여 -> 피보나치 수로 분해하여야 한다.
1-1. 분해된 피보나치 수의 이전 항을 구해야 한다.

문제 힌트:
n번째 피보나치 항을 여러 번 계산한다고 해서 그 값이 달라지지 않는다. 즉, 한번 구한 항을 기록(memoization) 해 둔 다음, 그 값이 필요할 때 꺼내쓴다.

알고리즘:
[나무위키 출처]
def FibonaChicken(N):
    if N <= 2:
        return 1
    i = inverse_fibonacci(N)
    if is_fibonacci(N):
        return Binet(i - 1)
    else:
        while N > Binet(i):
            i += 1
        return Binet(i - 2) + FibonaChicken(N - Binet(i - 1))

