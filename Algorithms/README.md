# Algorithms

## Big O

Big O 표기법은 불필요한 연산을 제거하여 알고리즘 분석을 쉽게하기 위한 표기법

- O(1) 제일빠름
- O(log n)
- O(n)
- O(n log n)
- O(n^2)
- O(2^n)
- O(n!) 제일늦음 숫자커지면 계산 불가

![image of Big O](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdqt3XN%2FbtqxKAwgT7d%2FKrLD2p4Ea1VeKzj8jkuLN0%2Fimg.jpg)

아래는 시간복잡도를 Big O 표기법으로 변환하는 것이다.

```
1 -> O(1)
2n + 20 -> O(n)
n^2+n => O(n^2)
n^3+n^2 => O(n^3)
```

Big O의 종류별 코드

## O(1)

```javascript
function o1(n) {
  return n;
}
```

## O(log n)

```javascript
/*
  arr는 숫자가 정렬된 Array 라는 가정
  주어진 array에 n의 인덱스를 찾는 함수
  arr 안에 입력한 n이 무조건 전대한다는 조건입니다.
  배열에서 값을 찾을 때 중간값 기준으로 낮은쪽 높은쪽을 선택하므로 시간이 두배로 줄어들어 O(log n)
*/
function onlogn(arr, n) {
  let nowIndex = Number((arr.length - 1) / 2);
  while (true) {
    if (arr[nowIndex] > n) {
      nowIndex = Number(nowIndex / 2);
    } else if (arr[nowIndex] < n) {
      nowIndex = nowIndex + (arr.length - 1 - nowIndex) / 2;
    } else {
      return nowIndex;
    }
  }
}
```

## O(n)

```javascript
function on(n){
    let asterisk ='';
    for(let i=0; i<n i++){
        asterisk += '*';
    }
    return asterisk;
}
function on2(n){
    let asterisk ='';
    for(let i=0; i<n i++){
        for(let j=0; j<3; j++){
            asterisk += '*';
        }
    }
    return asterisk;
}
```

## O(nm)

```javascript
function on(n, m) {
  let asterisk = "";
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < m; j++) {
      asterisk += "*";
    }
  }
  return asterisk;
}
```

## O(n log n)

- 합병정렬, 퀵정렬, 힙정렬

## O(n^2)

```javascript
function on2(n, m) {
  let asterisk = "";
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < n; j++) {
      asterisk += "*";
    }
  }
  return asterisk;
}
```
