[환경설정] (필수) Scoop 설치

> 윈도우 패키지 매니저인 scoop을 설치 한다.
> 모든 단계는 [bemantakumi](https://okky.kr/user/info/4562)님의 
>
> OKKY [개발툴 및 어플을 편하게 설치 해주는 scoop 커멘드라인 인스톨러 ](https://okky.kr/article/592228)의 글을 거의 
> 그대로 참조 함.



###### Phase01.  Powershell 관리자 권한으로 오픈

###### Phase02.  스쿱설치에 필요한 권한 주기

```bash
$> Set-ExecutionPolicy RemoteSigned -scope CurrentUser 
```

###### Phase03.  스쿱 설치

```bash
$> iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

###### Phase04.  필수 유틸 설치

> 문서에는 `7zip busybox openssh openssl git aria2 `를 설치하라고 나오는데
> 여기서 제일 필수는 `git`이다. 그냥 `git`만 설치 해도 크게 상관 없다.

```bash
$> scoop install git
```

###### Phase05. 별도 유틸등을 설치하기 위한 엑스트라 버킷 추가

```bash
$> scoop bucket add extras
```

###### Phase06. ruby, npm등의 버전을 골라 쓸 수 있게 해주는 버전 버킷 추가

```bash
$> scoop bucket add versions
```

###### Phase07.  자바 버킷은 필요할때 설치

> 단 오라클jdk8을 쓰는 경우 직접 설치

```bash
$>  scoop bucket add java
```









