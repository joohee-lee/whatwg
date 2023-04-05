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

```

IOS 10 부터는 use-scalble=no 속성 적용되지 않음. 

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


