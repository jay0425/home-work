# 메뉴 드롭다운하기

<p align="center"><img src="./3차과제이미지.gif" width="400" height="400"></p>

https://jay0425.github.io/home-work/mission-03/transition

<br>

# html

```html
<header>
  <h2>관련<span>사이트</span></h2>
</header>
```

<br/>

- 헤더의 h2에서 '사이트'부분은 따로 색깔과 마진을 주기 위해 span 태그로 감쌌습니다.

<br/>

```html
<main>
  <div class="menu">
    <ul>
      <li><a href="#">제로베이스</a></li>
      <li><a href="#">W3C</a></li>
      <li><a href="#">데이원 컴퍼니</a></li>
      <li><a href="#">웹 접근성 연구소/a></a>li></li>
      <li><a href="#">MDN</a></li>
    </ul>
  </div>
</main>
```

<br/>

- 메뉴의 가장 바깥 자리는 main 태그로 감쌌습니다.
- 메뉴의 컨텐츠들은 ul태그안에 li태그로 넣었습니다.

<br/>

# CSS

```css
main {
  width: 100%;
  height: auto;
  background: #ffffff;

  border: 0.1rem solid #a3a3a3;
  border-radius: 0.5rem;

  box-sizing: border-box;

  overflow: hidden;
}
```

<br>

- 메인 태그에서 overflow에 hidden을 줘서 ul태그의 첫째 li만 보이고 나머지 li들은 보이지 않게 하였습니다.

<br>

```css
.menu:first-child {
  transition: height 1s ease-in-out;
}
```

<br>

- 첫째 li에서 transition을 설정했습니다.

<br>

```css
.menu:hover {
  height: 15rem;
}
```

<br>

- 메뉴에 호버 시 세로 길이가 길어지게 설정했습니다.
