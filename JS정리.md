# 프로그래밍 언어의 기본 요소
1. 변수
2. 함수
3. 제어문(조건문)
4. 반복문

## 변수에 대해 알아보자
1. 변수는 primitive type 과 reference type이 있다.
2. primitive type: Number, String, Boolean, null, undefined 
3. reference type: Object(Array, Function, RegExp)

## 함수에 대해 알아보자
~~~js
// 1. 함수선언문
fn(); // 함수선언문은 Hoisting(끌어올림)대상이므로 실행된다.
function fn() {
	console.log("선언된 함수");
}

// 2. 함수표현식
fn2(); // 변수로 선언된 함수는 Hoisting 대상이 아니므로 에러가 난다.
var fn2 = function() {
	console.log("표현된 함수");
}

// 3. 함수의 이해
// 함수는 함수명() <-- 가로를 열고 닫아야 실행된다.
~~~
## 조건문과 반복문은 index12-정리 참조

# jQuery 배워야 할 것
## 접근자 - $("객체명")
index(), eq(), find(), children(), sibling(), parent(), next(), prev()

## 이벤트
click, mouseover, mouseleave, scroll, resize, keypress, keyup
on(), off(), one(), trigger(), delegate(), undelegate(), live(), die()

## Animation
1. animate({css}, 속도, easing, cb)
2. fadeIn(), fadeOut(), fadeToggle() 
3. hide(), show(), toggle()
4. slideUp(), slideDown(), slideToggle()
5. stop(), delay(), clearQueue()

## DOM
1. 생성
append(), appendTo(), prepend(), prependTo(), clone(), html(), text(), insertAfter(), insertBefore(), after(), before(), wrapAll(),
2. 삭제
empty(), remove()
3. 반복: each()

## css관련
1. addClass(), removeClass(), toggleClass(), hasClass();
2. css("color"), css({"color": "red"}), css("color", "red")
~~~js
var color = $(".box").css("color"); // Getter
$(".box").css({"color": "red"}) // Setter
~~~

## 속성관련
1. attr("src"), attr("src", "./img/a.jpg"), data(), prop()