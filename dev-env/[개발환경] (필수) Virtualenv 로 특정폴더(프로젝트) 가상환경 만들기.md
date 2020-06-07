#### [환경설정] (필수) Virtualenv 로 특정폴더(프로젝트) 가상환경 만들기

> [파이썬 초심자를 위한 PIP 그리고 Virtualenv 소개](https://medium.com/@dan_kim/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%B4%88%EC%8B%AC%EC%9E%90%EB%A5%BC-%EC%9C%84%ED%95%9C-pip-%EA%B7%B8%EB%A6%AC%EA%B3%A0-virtualenv-%EC%86%8C%EA%B0%9C-a53512fab3c2) :thumbsup:
>
> ```
> virtualenv는 아주 구체적인 문제를 해결합니다.
> 보통 여러개의 파이썬 프로젝트가 하나의 컴퓨터에서 충동을 일으키지 않고 존재할 수 있도록 도와줍니다.
> ```
>
> ```
> virtualenv는 각 프로그램별로 완전히 독립적인 가상의 환경을 만들어냄으로서...
> ```
>
> virtualenv는 각 프로젝트별 독립된 환경을 만들어준다.
> 이것이 필요한 이유는 위의 글을 잘 읽어보면 된다. 지금 완전히 모른 상태에서
> 안답시고 글을 쓰는 것은 나중에 더 큰 혼란을 초래하고, 제대로 안상태라는 가정에서
> 이 글을 업그레이드 해주길 바래 ~



###### Phase01.  virtualenv 설치

> virtualenv를 사용하기 위해서는 pyenv를 설치 해야 합니다.

```bash
$> git clone https://github.com/yyuu/pyenv-virtualenv.git ~/.pyenv/plugins/pyenv-virtualenv
$> echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
$> source ~/.bashrc
```



###### Phase02.  명령어를 통한 가상환경 생성/삭제, 적용/해제

```bash
# 가상환경 만들기
$> pyenv virtualenv 3.8.2 {환경 이름}
   => 보통은(정말?) 프로젝트 이름으로 환경이름을 만든다.

# 가상환경 삭제
$> pyenv virtualenv-delete {환경 이름}

# 가상환경 구동!!
$> pyenv activate {환경 이름}

# 구동 후 커맨드라인
({환경 이름}) $> _
```

> 주의!!. 현재 pyenv 버전(1.2.18-19-gcf81e5a0)에서 `pyenv activate` 명령어를
> 실행시키면,
>
> ```bash
> pyenv-virtualenv: prompt changing will be removed from future release. configure `export PYENV_VIRTUALENV_DISABLE_PROMPT=1' to simulate the behavior.` 
> ```
>
> 라는 경고 메시지가 나오는데 다음 버전으로 릴리즈 되면 프롬프트 앞 환경이름은 없어 진다라는 이야기  `export PYENV_VIRTUALENV_DISABLE_PROMPT=1`을 환경설정에 집어 넣고 시뮬레이션 해보면 환경을 적용 후 프롬프트에 환경이름이 사라지는걸 볼 수 있다.



#### 끗~~