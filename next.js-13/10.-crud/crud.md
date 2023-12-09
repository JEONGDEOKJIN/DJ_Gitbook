# 10. \[CRUD] 글 목록 가져오기

### 기본 개념

* 기본 ![](https://i.imgur.com/VslbOsX.png)

```bash
- server component 와 clinet component 는 '사용할 수 있는 api' 가 '다름' ⭐⭐⭐ 

- 기본은 서버 컴포넌트 
```

* 언제 서버 컴포넌트 vs 클라이언트 컴포넌트

```bash
- '단순히 정보를 보여주면' -> '서버 컴포넌트'
- '사용자와 상호작용' (interactive UI) 면 -> 클라이언트 컴포넌트
```

(- 아래와 같이, 그림을 보고, 이해하니까 좋다 ⭐⭐⭐⭐⭐⭐ ) ![](https://i.imgur.com/8ArRPc1.png)

### 클라이언트 컴포넌트 에서 js 여부에 따라서 달라지는 경우

#### hydration 예시

**js 없이 실행되는 경우 (정적 html 만 되는 경우) ⭐⭐⭐⭐⭐⭐ #js가없는경우예시 #hydrattion**

```
js 를 끄면 -> 서버와 통신하는 useEffect , fetch 같은 함수가 실행되지 않음 -> 서버에서 데이터를 가져오지 못 함
```

![](https://i.imgur.com/df0BYct.png)

**js 있는 경우 -> 이 순간 hydration 이지 않을까?**

```bash
1. useEffect 에서 fetch 를 사용해서, '서버에서 data 를 가져온다.' (fetching)
2. useState 에 저장한다. (상태관리)
3. 저장된 걸, html 에 뿌려준다. (렌더링)
```

\


### 클라이언트 컴포넌트를 서버 컴포넌트로 변환해보기 ⭐⭐⭐⭐⭐⭐

1. 문제 상황

```bash
이 코드의 문제는 뭘까? 

즉, 
'data fetching -> 상태관리 활용해서 data 저장 -> html 에 꽂아서 그리기' 의 흐름을 나타낸다. 

이때, 
next.js 는 서버 자원 (서버 api, 서버 data 등) 을 활용해서 먼저 그릴 수 있는 것은 그려주고 
브라우저 자원(브라우저 api, 브라우저 js 환경) 을 활용해서 그려야 하는 것은, client 컴포넌트로 변환하길 강요한다. 요구한다.

그러면, 고민해야 하는 건, 이 컴포넌트를 그릴 때, 브라우저 자원이 필요한건가? 를 판단해야 한다. 
왜냐면, 컴포넌트는 기본적으로 '서버 컴포넌트' 이므로.

이것을 기준으로 코드가 나뉘어지게 된다.
하나의 기준을 next.js 가 제시한 것. 
```

![](https://i.imgur.com/rUy7qBv.png)

CF. 추가적인 생각

```
서버 컴포넌트는 한번 렌더링 되고, 클라이언트에게 전달하는 역할만 하면 됨 | 자, 그러면, 각자의 역할을 나눠서 작성해야 함 ⭐⭐⭐⭐⭐⭐ 
```