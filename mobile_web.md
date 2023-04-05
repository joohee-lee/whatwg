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
  
>
```
