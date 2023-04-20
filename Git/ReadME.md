# Git
- 소프트웨어 개발 및 소스코드 관리에 사용
- 로컬에서 버전관리를 하지만 다른 사람과 실시간으로 코드를 공유할 수 없다.

# Github--Origin
- 클라우드 저장소
- git repository를 위한 웹기반 호스팅 서비스
- 클라우드 서버를 사용하여 로컬에서 관리한 코드를 업로드하여 공유할 수 있다.

# Git의 작업 영역
- working directory
- staging area(index영역)
- repository

1. 유저 이름 설정
```
git config --global user.name "your_name" 
```

2. 유저 이메일 설정하기
```
git config --global user.email "your_email"
```

3. 정보 확인하기
```
git config --list
```

# Github에 처음 코드 업로드하기
1. 초기화
```
git init
```

2. 추가할 파일 더하기
```
git add .
```
. 은 모든 파일이라는 뜻, 선택적으로 올리고 싶으면 add뒤에 파일 이름을 붙여주면됨(ex, git add index.html)
<br/><br/>


3. 상태 확인
```
git status
```

4. 히스토리 만들기
```
git commit -m "first commit"
```
-m은 메세지의 줄인말, 하고싶은 말을 쓰면됨
<br/><br/>

5. Github repository랑 내 로컬 프로젝트랑 연결
```
git remote add origin "깃허브 주소" (깃허브주소 복붙하기)
```

6. 잘 연결됐는지 확인(선택사항)
```
git remote -v
```
내가 연결한 주소값이 잘 뜨면 성공
<br/><br/>

7. Github로 올리기
```
git push origin master
```
master 자리에는 branch이름이 들어가면 됨, branch 이름이 main이라면 git push origin main이라고 써야함
