#### [환경설정] (필수) Autoenv로 프로젝트 폴더 진입시마다 자동으로 환경설정



###### Phase01. autoenv 설치

```bash
$> git clone git://github.com/kennethreitz/autoenv.git ~/.autoenv
```



###### Phase02. (선택) 기본환경 파일 이름 변경

> autoenv는 폴더에 진입시 .env 파일을 읽어 그 안의 스크립트를 실행한다.
> 하지만 `.env` 파일은 다른곳에서도 사용되는 경우가 있어 `.autoenv` 같은 다은 이름을
> 읽을 수 있도록 환경 설정을 한다.

```bash
# auto env 파일 이름을 자동에서 커스텀하게 설정
# 주의! 'source ~/.autoenv/activate.sh' 설정 이전에 한다.
$> echo 'export AUTOENV_ENV_FILENAME=".autoenv"' >> ~/.bashrc

$> echo 'source ~/.autoenv/activate.sh' >> ~/.bashrc
```



###### Phase03. 프로젝트 폴더에 `.autoenv` 파일을 만들고 아래와 같이 기입한다.

```bash
echo "python pyenv > {프로젝트 폴더} 진입"
pyenv shell {환경 이름}
pyenv activate
```

> 파일 생성 후 다시 그 폴더에 진입시 아래와 같은 문구가 나오고 `y`를 눌러 허용하면
> 설정된 환경으로 진입한다.

```bash
$ cd sample-virtualenv/
autoenv:
autoenv: WARNING:
autoenv: This is the first time you are about to source /mnt/d/projects/A-BOWL-OF-DJANGO-TODO-LIST/sample-virtualenv/.autoenv:
autoenv:
autoenv:   --- (begin contents) ---------------------------------------
autoenv:     echo "python pyenv > sample-virtualenv M-lM-'M-^DM-lM-^^M-^E"$
autoenv:     pyenv shell sample-virtualenv$
autoenv:     pyenv activate$
autoenv:
autoenv:   --- (end contents) -----------------------------------------
autoenv:
autoenv: Are you sure you want to allow this? (y/N) y
python pyenv > sample-virtualenv 진입

$> python --version
Python 3.6.2  => sample-virtualenv 환경에 설정된 파이선 버전
```

