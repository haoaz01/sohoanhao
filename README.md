# sohoanhao
import random

def check_perfect_number(n):
    factors = []
    for i in range(1, n):
        if n % i == 0:
            factors.append(i)
    if sum(factors) == n:
        return True
    else:
        return False

def random_perfect_number():
    while True:
        num = random.randint(1, 10000)
        if check_perfect_number(num):
            return num

perfect_number = random_perfect_number()
print("Số hoàn hảo ngẫu nhiên là:", perfect_number)
