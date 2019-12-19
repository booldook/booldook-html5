# HTML(HyperText Markup Language) 정리
~~~html
<!-- 기본태그 - block -->
<div>한 줄(block)을 차지</div>
<ul>
	<li>리스트표현</li>
	<li>리스트표현</li>
</ul>
<ol>
	<li>순서가 있는 리스트 표현</li>
	<li>순서가 있는 리스트 표현</li>
</ol>
<!-- form은 [block] / input, select... [inline-block] -->
<form>
	<input type="text" >
</form>

<!-- Headline 및 본문 -->
<!-- h1 ~ h5 : h1이 가장 크고 h5가 가장 작다./bold체로 표현 -->
<!-- p : 본문의 문단을 표현 -->
<h1>Headline1</h1>
<h2>Headline2</h2>
<h3>Headline3</h3>
<h4>Headline4</h4>
<h5>Headline5</h5>
<p>단락(문장)을 표현</p>

<!-- Semantic(의미론) tag - div의 속성을 가짐 /HTML5 -->
<header>네비게이션, 로고등을 감싸서 상단에 위치</header>
<section>본문내용</section>
<footer>저작권, 연락처 등 하단에 위치</footer>
<aside>광고, 링크</aside>
<main>배너, 메인내용</main>
<nav>네비게이션</nav>
<pre>
쓴대로 나와요.
		space, tab, enter 등이 적용된 상태로 그대로 나온다.
</pre>


<!-- 기본태그 - inline  -->
<span class="txt-red">Inline안에서 영역을 선택할 때</span>
<a href="./sub.html" target="_blank">글씨로 취급(inline)</a>
<img src="./img/p1.jpg">
<b>글씨가 두꺼워집니다. css의 [font-weight: bold]</b>
<i>글씨가 누워요</i>
<br> <!-- 한줄을 띄워줘요 -->
&nbsp; <!-- 한칸을 뛰워줘요 -->

~~~