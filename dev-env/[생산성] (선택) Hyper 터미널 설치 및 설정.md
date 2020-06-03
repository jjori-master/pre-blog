#### [생산성] (선택) Hyper 터미널 설치 및 설정

> 전호진님의 [Windows10에서 Linux 개발환경 구축 ](https://crynut84.github.io/2018/01/10/building-dev-env-using-wsl/)을 참조하여 작성된 글입니다.
>
> [공식사이트](https://hyper.is/), [awesome-hyper](https://github.com/bnb/awesome-hyper)



###### Phase01. Scoop을 통해 hyper 설치

> 설치에 여러가지 경로가 있겠지만 윈도우는 scoop을 통해 손쉽게 설치가 가능하다

```bash
$> scoop install hyper
```



###### Phase02. 최고 기본 설정

> Hyper 실행 후 단축키 `Ctrl + ,` 를 누르면 설정영역이 나오는데
> shell 과 shellArgs를 아래와 같이 설정한다.

```json
shell: 'C:\\Windows\\System32\\cmd.exe',
shellArgs: ['--login', '-i', '/c wsl'],
```

> 설정 후 다시 실행하면 `넌 이미 wsl에 접속해 있다~!!`