# Page 2

## 흐름

## 사용 할 수 있는 메소드

### 1. includes

```js
1. '숫자 하나' 를 찾는 경우 
const array1 = [1, 2, 3];
console.log(array1.includes(2));    // true 반환

2. '문자 하나' 를 찾는 경우
const pets = ['cat', 'dog', 'bat'];
console.log(pets.includes('cat'));    // true 반환

3. '연속된 문자' 가 있는지 여부 
ab6CDE443fgh22iJKlmn1o.includes('6CD')    // true 반환
ppprrrogrammers.includes('pppp')    // false 반환

```

* 관련문제 \[\[230915\_코딩테스트#문제 3 문자열 안에 문자열]]

### 2. indexOf

```js
const beasts = ['ant', 'bison', 'camel', 'duck', 'hello' , 'bison'];

// 전제 beasts 배열 중 '첫 번째 bison' 이 '몇 번째 있는가'
  // ⭐⭐ 인덱스 5번째 bison 은 무시함 ⭐⭐
document.writeln(beasts.indexOf('bison'));        // 1

// 인덱스 2 부터 시작했을 때, bison 이 전체 몇 번째 index 에 있는지 여부
document.writeln(beasts.indexOf('bison' , 2));    // 5

// 찾고자 하는 값이 없는 경우 👉 -1
document.writeln(beasts.indexOf('123'));    // -1
```



See the Pen [indexOf 메소드](https://codepen.io/anotheryear-hm/pen/WNLERKJ) by JeongDeokjin ([@anotheryear-hm](https://codepen.io/anotheryear-hm)) on [CodePen](https://codepen.io).

See the Pen \<a href="https://codepen.io/anotheryear-hm/pen/WNLERKJ"> indexOf 메소드\</a> by JeongDeokjin (\<a href="https://codepen.io/anotheryear-hm">@anotheryear-hm\</a>) on \<a href="https://codepen.io">CodePen\</a>.





```
const beasts = ['ant', 'bison', 'camel', 'duck', 'hello' , 'bison'];
// 전제 beasts 배열 중 '첫 번째 bison' 이 '몇 번째 있는가'
// ⭐⭐ 인덱스 5번째 bison 은 무시함 ⭐⭐
document.writeln(beasts.indexOf('bison'));        // 1
// 인덱스 2 부터 시작했을 때, bison 이 전체 몇 번째 index 에 있는지 여부
document.writeln(beasts.indexOf('bison' , 2));    // 5
// 찾고자 하는 값이 없는 경우 👉 -1
document.writeln(beasts.indexOf('123'));    // -1
```



{% embed url="https://codepen.io/anotheryear-hm/pen/WNLERKJ?editors=1010" %}

{% embed url="https://codepen.io/anotheryear-hm/pen/WNLERKJ" %}

See the Pen [indexOf 메소드](https://codepen.io/anotheryear-hm/pen/WNLERKJ) by JeongDeokjin ([@anotheryear-hm](https://codepen.io/anotheryear-hm)) on [CodePen](https://codepen.io).



* 코드펜

See the Pen \<a href="https://codepen.io/anotheryear-hm/pen/WNLERKJ"> indexOf 메소드\</a> by JeongDeokjin (\<a href="https://codepen.io/anotheryear-hm">@anotheryear-hm\</a>) on \<a href="https://codepen.io">CodePen\</a>.
