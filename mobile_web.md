# 모바일 웹 코딩

## tip 

1. body {-webkit-text-size-adjust: none}

```

html, body{
  -webkit-text-size-adjust : none;  /* 크롬, 사파리, 오페라 신버전 */
  -ms-text-size-adjust : none;  /* IE */
  -moz-text-size-adjust : none;  /* 파이어폭스 */
  -o-text-size-adjust : none;  /* 오페라 구버전 */
}
 
 
1) 화면의 폭에 맞춰어서 텍스트의 크기를 자동 조절
-webkit-text-size-adjust: auto; 

2) 폰트사이즈 고정
-webkit-text-size-adjust: none;

3) 폰트사이즈 지정된 사이즈로 변경 
-webkit-text-size-adjust: n%; 

```


2. viewport 모바일 웹페이지 가로 크기에 맞추기 

```
<meta 
  name="viewport" 
  content="width=device-width,
  initial-scale=1.0,
  minimum-scale=1.0,
  maximum-scale=1.0,
  user-scalable=no"> 
  
width=device-width : 플랫펌 가로 크기에 맞춤
initial-scale : 확대비율
maximun-scale : 최대확대비율
minimum-scale=1.0 : 최소축소비율
user-scalable : 사용자에 의한 화면 확대 기능 여부(yes/no)

참고) IOS 10 부터는 use-scalble=no 속성 적용되지 않음. 

```


3. 웹페이지가 브라우징된 후, 주소창 사라지게 

```
window.addEventListener('load', function() {
    setTimeout(scrollTo, 0, 0, 1);
}, false);

```

4. userAgent / 기기 체크 

```

```

5. background-image 를 넣을 경우, background-size 사용 

```
.bg {background: url(bg.png) no-repet 0 0; background-size: 100% 100%;}

```

6. 이미지 해상도 맞게 조절 하고 싶을 경우 

```

.a {width:auto;}
.a img {max-width: 100%};

```

7. width값이 100%인 경우 border 값을 넣으면 가로스크롤이 생겨 버림 

8. select, input등에 원치않는 그라데이션과 라운드가 처리되어 있는데, 이 form 요소의 기본속성을 초기화

```
 " -webkit-appearance:button; border-radius:0 "
 
 
input[type='text'],
input[type='password'],
input[type='submit'],input[type='search'] {
-webkit-appearance:none; border-radius:0
}

input:checked[type='checkbox'] {
  background-color:#666; 
  -webkit-appearance:checkbox
 }

button,
input[type='button'],
input[type='submit'],
input[type='reset'],
input[type='file'] {
  -webkit-appearance:button; border-radius:0
 }
input[type='search']::-webkit-search-cancel-button {-webkit-appearance:none}


```

9. pc reset css

```
/* reset */
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,textarea,p,blockquote,th,td,input,select,textarea,button {margin:0;padding:0}
fieldset,img {border:0 none}
dl,ul,ol,menu,li {list-style:none}
blockquote, q {quotes: none}
blockquote:before, blockquote:after,q:before, q:after {content:'';content:none}
input,select,textarea,button {vertical-align:middle}
button {border:0 none;background-color:transparent;cursor:pointer}
body {background:#fff}
body,th,td,input,select,textarea,button {font-size:12px;line-height:1.5;font-family:'돋움',dotum,sans-serif;color:#333} /* color값은 디자인가이드에 맞게사용 */
a {color:#333;text-decoration:none}
a:active, a:hover {text-decoration:underline}
address,caption,cite,code,dfn,em,var {font-style:normal;font-weight:normal}

```

10. mobile reset css 


- 버전 1


```
/* reset */
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,textarea,p,blockquote,th,td,input,select,textarea,button {margin:0;padding:0}
fieldset,img {border:0 none}
dl,ul,ol,menu,li {list-style:none}
blockquote, q {quotes:none}
blockquote:before, blockquote:after,q:before, q:after {content:'';content:none}
input,select,textarea,button {font-size:100%;vertical-align:middle}
button {border:0 none;background-color:transparent;cursor:pointer}
table {border-collapse:collapse;border-spacing:0}
body {-webkit-text-size-adjust:none} /* 뷰표트 변환시 폰트크기 자동확대 방지 */
input[type='text'],input[type='password'],input[type='submit'],input[type='search'] {-webkit-appearance:none; border-radius:0}
input:checked[type='checkbox'] {background-color:#666; -webkit-appearance:checkbox}
button,input[type='button'],input[type='submit'],input[type='reset'],input[type='file'] {-webkit-appearance:button; border-radius:0}
input[type='search']::-webkit-search-cancel-button {-webkit-appearance:none}
body {background:#fff}
body,th,td,input,select,textarea,button {font-size:14px;line-height:1.5;font-family:'Malgun Gothic', '맑은 고딕', sans-serif;color:#333} /* color값은 디자인가이드에 맞게사용 */
a {color:#333;text-decoration:none}
a:active, a:hover {text-decoration:none}
address,caption,cite,code,dfn,em,var {font-style:normal;font-weight:normal}

```

버전 2

```

/* Reset */
html,body,h1,h2,h3,h4,h5,h6,div,p,blockquote,pre,code,address,ul,ol,li,menu,nav,section,article,aside,
dl,dt,dd,table,thead,tbody,tfoot,label,caption,th,td,form,fieldset,legend,hr,input,button,textarea,object,figure,figcaption {margin:0;padding:0;}

html,body{width:100%;}
/* -webkit : 크롬, ios기반의 브라우저 */
html{
  -webkit-touch-callout:none; // 비표준 , 브라우저에서 지원하지않음. 
  -webkit-user-select:none;
  -webkit-tap-highlight-color:rgba(0,0,0,0);}


/*

user-select 사용자가 텍스트를 선택할 수 있는지 지정

/* 키워드 값 */
user-select: none;
user-select: auto;
user-select: text;
user-select: contain;
user-select: all;

/* 전역 값 */
user-select: inherit;
user-select: initial;
user-select: unset;


*/

/*

-webkit-tap-highlight-color는 링크를 탭할 때 나타나는 강조를 설정하는 비표준 CSS 속성입니다.
강조는 사용자가 탭이 성공적으로 인식되고 있는지를 나타내며, 어떤 요소를 탭하고 있는지를 나타냅니다.

a {
    color: inherit;
    text-decoration: none;
    -webkit-tap-highlight-color: rgba(0, 0, 0, .1)
}

*/


/* 가로사이즈가 ios(iphone3 , gallaxy1은 가로가 320) | -webkit-text-size-adjust: 아이폰 가로/세로변경시 글씨 사이즈 제어*/
body{
  width:100%; 
  background:#fff; 
  min-width:320px; 
  -webkit-text-size-adjust:none;
  word-wrap:break-word;
  word-break:break-all;}
/* 웹용 */
body,input,select,textarea,button {border:none;font-size:12px;font-family: 'Noto Sans KR', sans-serif; color: #727272;}
/* 모바일 : 아이폰은 애플고딕, 안드로이드는 따로 폰트로 된다. */
body,input,select,textarea,button {border:none;font-size:12px; color: #727272;} 
ul,ol,li{list-style:none;}
table{width:100%;border-spacing:0;border-collapse:collapse;}
img,fieldset{border:0;}
address,cite,code,em{font-style:normal;font-weight:normal;}
label,img,input,select,textarea,button{vertical-align: middle;}
.hide,caption,legend{line-height:0;font-size:1px;overflow:hidden;}
hr{display:none;}
/* html5에서는 inline요소다 이것을 block으로 바꿔줌 */
main,header,section,nav,footer,aside,article,figure{display:block;}
a{color:#000; text-decoration:none;}


/* Form */
textarea {border:1px solid #dbdbdb;}
select { height:32px; font-size: 13px; color:#373737; border:1px solid #e9e9e9; background:#fff; border-radius:5px; }
input[type=tel],
input[type=time],
input[type=text],
input[type=password],
input[type=search],
input[type=email],
input[type=file],
input[type=url],
input[type=number],
input[type=date],textarea {
  width:100%; 
  height:30px; 
  font-size:13px; 
  color:#373737; 
  border:1px solid #e9e9e9; 
  background:#fff; 
  text-indent:20px; 
  border-radius:5px;
  transition:all 0.5s; 
  vertical-align:middle;}

/* placeholder는 직접 선택할 수 없어서 세팅해줌 */
input::-webkit-input-placeholder{ color:#b5b5b5; font-size:12px; line-height:100%;}
textarea{padding:5px 0;}
select:focus,
textarea:focus,
input:focus { border: 1px solid #727272; }

/* search 경우 클릭할때 둥글게 나오는 경우 있음 사각형으로 만듬input[type=password][disabled], */
input[type=tel][readonly],
input[type=text][readonly],
input[type=password][readonly],
input[type=search][readonly],
input[type=email][readonly],
input[type=tel][disabled],
input[type=text][disabled],
input[type=password][disabled],
input[type=search][disabled],
input[type=email][disabled] { 
  background:#eaeaea; border-color:#c0c0c0; color:#666; -webkit-appearance:none; font-size:12px;}
  
textarea[readonly],
textarea[disabled]{padding:11px; font-size:16px; color:#666; font-weight:normal; line-height:140%; height:78px; background:#eaeaea; border:1px solid #c0c0c0;}
.clear{clear:both;}
.clear:after {content:""; display:block; clear:both;}

```

11. 반응형 웹일 경우,  다행상도 대응 참고
```
'sm': '640px' // @media (min-width: 640px)
'md': '768px' // @media (min-width: 768px)
'lg': '1024px' // @media (min-width: 1024px)
'xl': '1280px' // @media (min-width: 1280px)
'2xl': '1536px' // @media (min-width: 1536px)

mobile: '360px' // @media (min-width: 360px)
foldable: '523px' // @media (min-width: 523px)
tablet: '768px' // @media (min-width: 768px)
'under-foldable': { max: '522px' } // @media (max-width: 522px)
'under-tablet': { max: '767px' } // @media (max-width: 767px)
'under-mobile': { max: '359px' } // @media (max-width: 359px)

```

12. iPhone X, iPhone 11의 안전영역(Safe area) 

