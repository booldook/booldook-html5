# css 정리
1. css(cascading style sheet)는 style sheet 라고 얘기함.
2. [inline방식 css적용.우선순위1] <div style="color: red;"></div>
3. [internal방식 css적용.우선순위2] html의 head안에서 <style></style>로 선언한다.
4. [external방식 css적용.우선순위3] html의 head안에서 <link rel="stylesheet" href="./css/index.css">
5. 우선순위 
	a. !important 10000점
	b. 인라인 스타일 1000점
	c. ID선택자 : 100점
	d. 클래스 선택자 : 10점 / 가상클래스(예:link) 10점
	e. 태그 1점 / 가상 엘리먼트 (예:first-child) 1점
6. 자식(자손)선택자
	a. div > ul <!-- 자식(바로밑에) 선택자 -->
	b. div ul <!-- 자손(내 안에있는 모든것) 선택자 -->
	c. div.wrap <!-- div들 중에 class가 wrap인 태그 -->

## CSS 선언
~~~html
<html>
	<head>
		<!-- 각종 링크 및 제목, meta정보를 기재하는 곳 -->
		<style>
			/* 이 영역은 css 영역입니다. */
		</style>
	</head>
	<body>
		<!-- HTML 본문 영역입니다. -->
	</body>
</html>
~~~

## CSS 속성
~~~css
/* 
css의 가장 중요한 개념들 
- display속성: block, inline, inline-block, none
- inline-block은 글씨속성(inline)을 가지지만 width, height, margin-top, margin-bottom 등 block만 가지는 속성도 가지게 된다.
- float: left, right
- float는 불안정한 상태 이므로 위치를 잡은 이후에 아래 태그에서 고정시켜줘야 함. (clear: both;)
*/

/* 기본 Block 속성 */
/* div(block을 대표하는 태그-속성없음) */
/* Semantic요소[header, section, footer, aside, nav] */

/* 기본 inline 속성 */
/* span(inline을 대표하는 태그-속성없음), a, b, img, i */

/* 글자와 관련된 속성 - 상속이 된다. */
color: #333;
font-size: 24px; /* 단위: px, %, rem, em, vw, vh ... */
text-decoration: none; /* underline, line-through ... */
font-family: 'Gulim', 'sans-serif';
font-weight: normal; /* normal, bold, 100, 200, 300... */
line-height: 1; /* 1, 1.5, 2, 30px... 줄간 */
letter-spacing: 5px;
text-align: center; /* left, right, center, justify */

/* 배경 */
background-color: red; 

/* 테두리와 관련된 속성 */
border: 1px solid red;
border-radius: 5px;
border-radius: 50%; /* 원을 만들때 */

/* 그림자와 관련된 속성 */
/* box-shadow: 좌우 상하 그림자Blur 색상(rgba) */
box-shadow: 4px 6px 10px rgba(0, 0, 0, 0.5);

/* 여백과 관련된 속성 */
margin: 12px; /* 상, 우, 하, 좌 12px */
margin: 12px 16px 20px 24px; /* 상(12px),우(16px),하(20px),좌(24px) */
margin: 12px 20px; /* 상하(12px), 좌우(20px) */
padding: 12px; /* margin과 주는방식이 똑같음 */

margin-left: 12px;
margin-top: 12px;
margin-right: 12px;
margin-bottom: 12px;

/* block을 문서의 가운데 정렬하려면 */
margin: 0 auto;

/* 크기(dimension)와 관련된 css */
box-sizing: content-box; /* (css 기본값) 테두리와 패딩을 제외한 실제 컨텐츠 영역의 크기로 width, height를 사용함 */
.box {
	/* 실제 width: 260px; 계산이 힘들다. */
	width: 200px; padding: 20px; border: 10px solid red;
}

box-sizing: border-box; /* (항상 이거로 써야함) 테두리와 패딩을 포함한 크기로 width, height를 사용함 */
.box {
	/* 실제 width: 200px; 계산이 쉽다. - 내용이 적용되는 영역: 140px; */
	width: 200px; padding: 20px; border: 10px solid red;
}

/* Position 정리 */
/* position은 absolute, relative, fixed, sticky 4가지 */
/* position 모델의 위치는 left, top, right, bottom이 있다. */
.box {
	position: fixed;
	/* fixed의 위치값의 기준점은 Browser이다. */
}
/* position: relative는 내 안에 있는 position모델의 기준점이 되어준다. */

/* FLEX 정리 */
justify-content (가로정렬)
- flex-start(기본:왼쪽정렬), 
- flex-end(오른쪽정렬), 
- 균등분할3형제- space-between, space-evenly, space-around

align-items (세로정렬)
- stretch(기본:늘리기), 
- flex-start(상단정렬), 
- flex-end(하단정렬),
- center(가운데정렬) 
~~~