#### Virtualenv 로 특정폴더(프로젝트) 가상환경 만들기

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

# 가상환경 만들기
$> pyenv virtualenv 3.8.2 {폴더 이름}

# 가상환경 삭제
$> pyenv virtualenv-delete {폴더 이름}

# 가상환경 구동!!
$> pyenv activate {폴더 이름}

# 구동 후 커맨드라인
({폴더 이름}) $> _

```



#### 끗~~





