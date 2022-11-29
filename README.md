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

4. git commit 남기기
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

### 2. Local Repository에서 Jekyll 시작 후 Remote Reposity에 반영

### 3. MongoDB 정리 업로드

### 4. Markdown 업로드

### 5. 테마 적용
