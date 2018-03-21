---
title: "How to make github post"
search: true
categories: 
  - github
  - markdown
last_modified_at: 2018-03-21T08:06:00-05:00
---

[Mike Lee](https://leemun1.github.io/ "Mike Lee")님의 [포스트](https://leemun1.github.io/webdev/2017/06/23/jekyll-github-pages-4/ "포스트")를 참고함.


# 1. 한글 웹폰트 적용하기

KoPub 돋움체의 주소를 가져와 적용하기
<pre><code>
/* KoPub Dotum */
@font-face {
  font-family: 'KoPub Dotum';
  font-style: normal;
  font-weight: 300;
  src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Light.eot);
  src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Light.eot?#iefix) format('embedded-opentype'),
       url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Light.woff) format('woff'),
       url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Light.ttf) format('truetype');
}
@font-face {
 font-family: 'KoPub Dotum';
 font-style: normal;
 font-weight: 400;
 src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Medium.eot);
 src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Medium.eot?#iefix) format('embedded-opentype'),
 url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Medium.woff) format('woff'),
 url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Medium.ttf) format('truetype');
}
@font-face {
  font-family: 'KoPub Dotum';
  font-style: normal;
  font-weight: 700;
  src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Bold.eot);
  src: url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Bold.eot?#iefix) format('embedded-opentype'),
       url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Bold.woff) format('woff'),
       url(//cdn.jsdelivr.net/font-kopub/1.0/KoPubDotum-Bold.ttf) format('truetype');
}
</code></pre>


적용 방법은 매우 간단하다. 위 코드를 CSS파일 내에 넣어준 후 (세가지 폰트 굵기 중 한가지만 선택하는것도 가능) font-family 속성에 폰트 이름을 써주시면 된다. 예를 들어 body 태그에 폰트를 지정하고 싶다면 다음처럼 코드를 작성하면 된다:
<pre><code>    
body {
    font-family: "PT Sans", Helvetica, Arial, "KoPub Dotum", sans-serif;
}
</code></pre>


영어와 한글에 각각 다른 폰트를 적용시키고 싶으면 font-family 속성 내에서 영문 폰트를 먼저 지정하여 영문 폰트에 우선순위를 주고 한글 폰트는 뒤쪽으로 배치한다. 또한 PT Sans 나 KoPub Dotum 과 같이 폰트 이름에 공백이 포함되어 있는 경우 쌍따옴표로 감싸주어야 한다. 


이미지 및 다운로드 가능한 파일 추가하기
포스팅 내에 이미지를 추가하려면 마크다운파일 내에 다음 코드를 적어주시면 됩니다.

![이미지 이름](이미지 주소)

제 경우 사이트내에서 사용될 이미지를 모두 저장소 내에 폴더를 따로 만들어서 관리하는데요 예를들어 저장소 내에 images 라는 폴더가 있고 그 안에 있는 cats.jpg 라는 파일을 추가하고싶다면 이미지 주소에

/images/cats.jpg

라는 링크를 적어주시면 됩니다. 이렇게 로컬 경로를 지정해도 되지만 웹에서 어떤 이미지를 가져오고싶다면 간단히 그 이미지 주소를 복사하여 똑같이 넣어주시면 됩니다. 이렇게 이미지를 추가할때는 이름앞에 느낌표를 붙혀준 반면 느낌표없이

[이름](주소)

의 형식을 따르면 링크가 됩니다. 따라서 파일을 추가하고싶다면 주소칸에 이미지를 추가할 때 처럼 파일이 위치한 로컬 경로를 지정해주거나 다른 어떤 외부 파일주소를 지정해주면 되겠죠. 예를들어 저장소 내 files 폴더에 들어있는 가이드.pdf 라는 파일을 다운받는 링크를 만들고 싶다면 다음과같이 링크를 작성해주시면 됩니다:

[가이드 다운로드](/files/가이드.pdf)
