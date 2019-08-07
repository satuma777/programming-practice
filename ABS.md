# [AtCoder Beginners Selection](https://atcoder.jp/contests/abs)

## [ABC086A - Product](https://atcoder.jp/contests/abs/tasks/abc086_a)

```python
a, b = map(int, input().split())
ret = 'Odd' if (a * b) % 2 == 1 else 'Even'
print(ret)
```



## [ABC081B - Shift only](https://atcoder.jp/contests/abs/tasks/abc081_b)

```python
N = input()
z = list(map(int, input().split()))
count = 0
flag = sum([i % 2 == 1 for i in z]) == 0
while flag:
  count += 1
  z = list(map(lambda x: x // 2, z))
  flag = sum([i % 2 == 1 for i in z]) == 0
print(count)
```



## [ABC087B - Coins](https://atcoder.jp/contests/abs/tasks/abc087_b)

```python
num_coins_500 = int(input())
num_coins_100 = int(input())
num_coins_50 = int(input())
target = int(input())
 
z = [
  [0 <= (target - (500 * i + 100 * j)) / 50 <= num_coins_50 for j in range(num_coins_100 + 1)] 
  for i in range(num_coins_500 + 1)
]
 
N = sum(list(map(sum, z)))
print(N)
```

