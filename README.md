## eun031006.github.io
> blog project 과정을 기술합니다.

### 1. Github Page 시작

1. eun031006.github.io 이름의 Repository 생성

2. Local-Remote Repository 연동

-Remote Repository 주소 복사
-git clone <repo_name><path>

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

### 4. Markdown 업로드

### 5. 테마 적용
