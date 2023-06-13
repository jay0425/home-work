# 그리드로 배치하기

<p align="center"><img src="./4차과제.png" width="400" height="300"></p>

<br>

https://jay0425.github.io/home-work/mission-04/grid

<br>

# html

```html
<div class="news">새소식</div>
<div class="more">더보기</div>
<div class="divider"></div>
```

- 새소식, 더보기, 줄을 위한 div를 작성했습니다.

```html
<figure class="img-wrapper">
  <img src="./news1.png" alt="W3C 리뉴얼 사진" class="img" />
  <figcaption class="img-title">W3C 리뉴얼</figcaption>
</figure>
```

- 이미지는 figure로 감싸줬고 아래에 figcaption으로 설명을 달았습니다.

```html
<article class="content">
  <header class="title">W3C 사이트가 리뉴얼 되었습니다.</header>
  <p class="date">2022.07.18</p>
  <p class="content">
    디자인 및 다양한 view 환경을 고려하여 구성되어 있으며, 기존보다 최신 정보 및 개발자를 위한 기술 가이드도 찾기 쉽도록
    구성되어 있습니다.
  </p>
</article>
```

- article 로 감싼뒤 헤더와 p 영역을 나누었습니다.

<br>

# CSS

```css
.container {
  width: 300px;
  height: 200px;

  display: grid;
  gap: 17px;
  grid-template-columns: repeat(7, 1fr);
  grid-template-rows: auto;
}
```

- 제일 바깥 태그인 container에서 grid 설정을 해주었습니다.

```css
.news {
  grid-row-start: 1;
  grid-column-start: 1;
  grid-row-end: 1;
  grid-column-end: 2;
  font-size: 14px;
  font-weight: 700;
  color: #ed552f;
  width: 37px;
}
```

- 새소식 부분의 그리드 설정입니다.

```css
.more {
  grid-area: 1 / 6 / 1 / 6;
  font-weight: 400;
  font-size: 14px;
  color: #000;
  width: 37px;
}
```

- 더보기 부분의 그리드 설정입니다.

```css
.divider {
  width: 266px;
  height: 1px;
  background: linear-gradient(90deg, #a9a9a9 -1.32%, #ffffff 100%);

  grid-area: 2 /1 / 2 / 9;
}
```

- 구분선의 그리드 설정입니다.

```css
.img-wrapper {
  grid-area: 3 /1 /4/ 2;
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: flex-start;
  width: 100px;
}
```

- 이미지 부분의 그리드 설정입니다.

```css
.content {
  grid-area: 3 /2 /4 / 8;
  font-weight: 400;
  font-size: 14px;

  width: 251px;
  height: 84px;
}
```

- article 부분의 그리드 설정입니다.
