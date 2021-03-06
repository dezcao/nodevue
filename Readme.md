### Node.js
```sh
모듈을 제공하는 쪽은 export
받는 쪽은 require로 받는다.
node.js는 파일시스템에 관해서 기본제공하는 라이브러리가 포함되어 있다.
그래서 별도 모듈 설치없이 바로 받겠다고 해주면 된다. require('fs');
```

### 그밖에 거의 필수적인 모듈들 설치해준다.
```sh
 npm i express (express-koa, 경량화 시켜준것도 있다.)
 npm i ejs
 npm i body-parser (리퀘스트의 파라미터 파싱용)
 npm i mysql
 npm i nodemon -g (개발중 자동 재시작 해줌.)
 npm i bluebird --save (connection pool, transaction, Kludgy)

 모듈들 제거 후 다시 깔때
 rm -rf node_modules/
 rm -rf dist
 npm i
```

### 형상관리
```sh
git 설치 후, 관리하고 싶은 프로젝트의 디렉토리로 이동. 

git init
git config --global user.name "이름"
git config --global user.email dezcao@naver.com
git config --list
git status

git add README (git add는 파일의 상태를 추적 + 수정한 파일을 Staged 상태만듬.)
git remote add origin 깃주소(https) ***
git remote remove origin (잘못해서 지울때) * 

clone 해오기
git clone git://github.com/schacon/grit.git

git pull
git push
git commit -a (add 수고를 덜기위해서 옵션 -a)

참고로 처음 설치했으면 visual studio code 재시작 해줘야 한다.
```

### .gitignore
```sh
cat .gitignore (무시할 파일을 만들어준다. window라면 cat 대신 type)
node_modules를 추가하여 불필요한 업로드를 없앤다.
git pull을 한경우 최초 npm install 한방이면 모두 설치될 것이다.
ignore는 항상 최상위 Directory에 존재해야한다.
```

### 참고, 형상관리 툴별 특징
```sh
csv (Concurrent Versions System) : 버전 분기가 힘들고, 장기간 분기된 버전 운영에 대해서 설계되지 않았음
svn (Apache Subversion) : 버전 분기가 개선되었지만 느림.
git : 리눅스 상에서 가장 빠른 속도, 인터넷 연결이 없을 때도 유용 
      단, SVN 보다 어렵고, 개별개발자 보다는 팀에 더 적합하고, 윈도우즈에선 리눅스보다 제한적이라 함.
```

### 프로그램 실행해 보기
```sh
node index.js
```

### visual studio code 단축키
```sh
멀티라인 선택 : ctrl + alt + 화살표 위, 아래 
커서의 라인삭제 : ctrl + X
```

### 세팅순서
```sh
visual studio code 설치 
    https://code.visualstudio.com/docs/?dv=win


visual studio code 세팅 변경
    view > toggle render whitespace

node.js 설치
    https://nodejs.org/ko/
    
git 프로젝트 가져올 폴더 만들기

git 설치
    https://git-scm.com/download/win
    git init
    git config --global user.name dezcao
    git config --global user.email dezcao@naver.com
    git clone https://github.com/dezcao/nodevue.git

최초 가져왔으면 프로젝트에 필요한 의존 모듈들을 받는다.
npm install
```
