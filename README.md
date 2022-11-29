## eun031006.github.io
> blog project 과정을 기술합니다.
> [blog 주소](https://eun031006.github.io/)

### 1. Github Page 시작

1. eun031006.github.io 이름의 Repository 생성

2. Local-Remote Repository 연동

- Remote Repository 주소 복사
- git clone <repo_name><path>

3. index.html 작성
```
<!DOCTYPE html>
<html>
   <head>
     <title>Github Page Test</title>
   </head>
   <body>
     <h2>This is test page.</h2>
     <p>이 페이지가 잘 보인다면 성공!</p>
   </body>
</html>
```

4. commit 남기기
```
git add index.html
```

```
git commit -m "add: index.html"
```

5. git push 로 Remote Repository에 반영하기
```
git branch -M main
```

```
git push origin main
```

6. Github Page 설정 확인
Repository Settings > Pages > eun031006.github.io로 접속

7. index.html 입력 내용이 제대로 뜨는지 확인
   
![image](https://user-images.githubusercontent.com/106921541/204574603-8758f795-0781-4751-a71d-ff428306e9f5.png)

### 2. Local Repository에서 Jekyll 시작 후 Remote Reposity에 반영
   
1. Jekyll 설치 완료

2. 현재 디렉토리에 Jekyll 설치
```
jekyll new . --force
```
   
3. jekyll serve 실행 후, localhost:4000 접속
```
bundle exec jekyll serve
```
   
![image](https://user-images.githubusercontent.com/106921541/204571771-f1e48b69-7678-4862-a71c-22948c70baab.png)

기본 테마의 Jekyll 사이트 생성

4. _config.yml 파일에서 블로그 속성 관리
   
5. commit 남기기
```
git rm index.html
```
   
```
git add *
```
   
git rm/add 를 통해 변경사항 반영할 파일들 지정
   
```
git commit -m "add: jekyll on repository"
```
   
```
git push origin main
```
   
Rocal Repository의 commit 정보를 Remote Repository에 반영
   
6. eun031006.github.io에 반영된 결과 확인

### 3. MongoDB 정리 업로드

1. `Add file`에서 `Create new file` 선택하여 직접 생성  
   
2. `_posts`에 `YYYY-MM-DD-TITLE.md` 형식으로 지정
  
3. 생성한 `2022-11-20-MongoDB 정리.md`에 포스트 작성
```
---
layout: post
title: "MongoDB 정리"
date:   2022-11-20 20:24:09 +0900
categories: update
---
   
내용 작성
   
```

다음 형식으로 포스트 시작 후 내용 작성
   
4. `Commit new file`을 클릭하여 포스트 발행
   
### 4. Markdown 업로드
   
1. `Add file`에서 `Create new file` 선택하여 직접 생성  
   
2. `_posts`에 `YYYY-MM-DD-TITLE.md` 형식으로 지정
  
3. 생성한 `2022-11-29-Markdown.md`에 포스트 작성
```
---
layout: post
title: "Markdown"
date:   2022-11-29 20:00:09 +0900
categories: update
---
   
내용 작성
   
```

다음 형식으로 포스트 시작 후 내용 작성
   
4. `Commit new file`을 클릭하여 포스트 발행

### 5. 테마 적용

1. jekyll theme 고르기
[jekyll theme site](http://jekyllthemes.org/)
   
2. 테마 다운로드 후 복사하여 github.io 폴더에 붙여넣기

_posts 제외하고 테마를 덮여쓴다.
   
3. git rm/add 를 통해 변경사항 반영할 파일들 지정
   
4. Remote Repository에 git push 하기
   
### 6. 댓글 기능 추가
   
1. Disqus 가입

2. 블로그에 Disqus 반영

```
comment:
  provider: "disqus"
  disqus:
    shortname: "eun031006-github-io"
```

- _config.yml 에 다음 내용 추가

```
{% include post.html %}
<h2>Comments</h2>
<div id="disqus_thread"></div>
<script>
    /**
     *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT 
     *  THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR 
     *  PLATFORM OR CMS.
     *  
     *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: 
     *  https://disqus.com/admin/universalcode/#configuration-variables
     */
    let PAGE_URL = "{{site.url}}{{page.url}}"
    let PAGE_IDENTIFIER = "{{page.url}}"
    var disqus_config = function () {
        // Replace PAGE_URL with your page's canonical URL variable
        this.page.url = PAGE_URL;  
        
        // Replace PAGE_IDENTIFIER with your page's unique identifier variable
        this.page.identifier = PAGE_IDENTIFIER; 
    };
    
    (function() {  // REQUIRED CONFIGURATION VARIABLE: EDIT THE SHORTNAME BELOW
        var d = document, s = d.createElement('script');
        
        // IMPORTANT: Replace EXAMPLE with your forum shortname!
        s.src = 'https://eun031006-github-io.disqus.com/embed.js';
        
        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>
    Please enable JavaScript to view the 
    <a href="https://disqus.com/?ref_noscript" rel="nofollow">
        comments powered by Disqus.
    </a>
</noscript>
```

- _layouts/post.html 에 Disqus 홈페이지에서 복사한 Universal Code 추가 후 수정

- _posts 속 포스트에 `comments: true` 지정하여 댓글 허용

![image](https://user-images.githubusercontent.com/106921541/204600389-bf999c0e-a434-4c1c-8e82-fb24fd84bf97.png)

- 댓글 기능 추가된 결과 
