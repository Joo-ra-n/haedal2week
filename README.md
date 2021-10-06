# 파이썬 심화

## 탐색과 정렬

### 순차탐색(Sequential Search)이란?

데이터 리스트가 있을 때, 이 리스트의 처음부터 끝까지 하나씩 순차적으로 확인하여 찾고자 하는 데이터가 있는 지 탐색하는 방식. 단방향으로 탐색하기 때문에 선형 탐색(Linear Search)라고도 한다.

![img](https://blog.kakaocdn.net/dn/c590VM/btqt4y8JOTV/zdaZpXO9k4yAkMmktBxMkk/img.gif)

정렬되지 않은 데이터의 크기가 n개일 때 평균적으로 (n+1)/2 번의 비교를 하고, 최악의 경우에는 n번의 비교를 한다. 따라서 시간 복잡도는 O(n) 이라고 할 수 있다.

##### 코드예시

```python
# 리스트에서 특정 숫자 위치 찾기
# 입력: 리스트  a, 찾을 값 x
# 출력: 찾으면 그 값의 위치, 없으면 -1

def serach_list(a, x):
    n = len(a)                       # 입력 크기 n
    for i in range (0,n):       # 순차 탐색 @@@ 생성
        if x == a[i]:               # 리스트의 값이 x와 같으면
            return i                 # 리스트 내의 위치 반환
    return -1                       # 끝까지 탐색해도 없으면 -1 반환

test = [1, 4, 6, 7, 33, 101]

print(search_list(test, 7))      #3
print(search_list(test, 101))   #5
print(search_list(test,55))     #-1
```

리스트의 처음부터 끝까지 비교한다는 점에서 상당히 비효율적이지만, 정렬이 되어 있지 않은 데이터는 어쩔 수 없이 순차탐색을 사용해야 한다. 이를 위해 다양한 정렬 방법이 고안되었는데, 다음 사람이 해주겠지?ㅋㅋ

