자료구조 Queue
=============
자료구조 큐의 특징
-------------------
* 한쪽 끝에서만 자료를 넣고 한쪽 끝에서만 자료를 뺄 수 있는 자료구조
* 먼저 넣은 것이 가장 먼저 나오기 때문에 First In First Out(FIFO)라고도 한다.

* queue의 기본 연산
    * push 큐에 자료를 넣는 연산
    * pop 큐에서 자료를 빼는 연산
    * front 큐의 가장 앞에 있는 자료를 보는 연산
    * back 큐의 가장 뒤에 있는 자료를 보는 연산
    * empty 큐가 비어있는지 아닌지를 알아보는 연산
    * size 큐에 저장되어있는 자료의 개수를 알아보는 연산

파이썬에서의 queue
--------------------
* 파이썬에서는 queue 모듈을 통해서 queue를 구현할 수 있다.

```python
    import queue
    q = queue.Queue() # 큐 생성
    q.put('data')     # 큐 객체에 데이터 입력
    q.qsize()         # 큐 객체에 저장된 데이터 갯수
    q.get()           # 큐 객체에서 값을 출력
```

자료구조 Deque
=============
자료구조 덱(Deque)의 특징
-----------------------
* 양 끝에서만 자료를 넣고 양 끝에서 뺼 수 있는 자료구조이다.
* Double-ended queue의 약자이다.

*  Deque의 기본적인 연산
    * push_front: 덱의 앞에 자료를 넣는 연산
    * push_bakck: 덱의 뒤에 자료를 넣는 연산
    * pop_front: 덱의 앞에서 자료를 빼는 연산
    * pop_back: 덱의 뒤에서 자료를 빼는 연산
    * front: 덱의 가장 앞에 있는 자료를 보는 연산
    * back: 덱의 가장 뒤에 있는 자료를 보는 연산

파이썬에서의 deque
-----------------------
* collections.deque 의 메소드들
```python
    import collections
    deq = collections.deque() # 덱 생성
    deq.append('data')        # data를 덱의 오른쪽(마지막)에 추가해준다
    deq.appendleft('data')    # data를 덱의 왼쪽(맨 앞)에 추가해준다.
    deq.extend('data')        # iterable argument를 오른쪽(마지막)에 추가해준다.
                              # iterable argument란? 각 요소를 하나씩 반환 가능한 object를 말한다.
                              # 'data'의 경우 'd' 'a' 't' 'a' 로 반환 가능하다.
    deq.extendleft('data')    # iterable argument를 왼쪽(맨 앞)에 데이터를 추가해준다.
    deq.pop()                 # 오른쪽(마지막) 요소를 반환후 제거한다.
    deq.popleft()             # 왼쪽(맨 앞) 요소를 반환후 제거한다.
    deq.rotate(n)             # 덱의 요소들을 n값 만큼 회전해주는 메소드이다.
                              # n값이 음수면 왼쪽으로 회전하고 n값이 양수면 오른쪽으로 회전한다.
```