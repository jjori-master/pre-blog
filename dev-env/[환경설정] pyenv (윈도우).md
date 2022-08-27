

#### pyenv
>  다양한 파이썬 버전/배포판을 손쉽게 관리하기 위함.
>  Scoop 을 통한 pyenv 패키지가 설치 되었다고 가정합니다.

```bash
# 설치 가능한 파이썬 버전/배포판 내역을 다시 읽습니다.
pyenv update

# 설치 가능한 파이썬 버전/배포판 출력
pyenv install --list

# 지정 버전/이름의 파이썬을 설치
pyenv install 3.10.6

# 지정 버전을 디폴트(글로벌) 버전으로 설정
pyenv global 3.10.6

# (파워쉘 고유명령) python 경로가 pyenv 내에 있음을 확인
get-command pyenv
python --version
> Python 3.10.6

# 혹은 특정 프로젝트에서 다른 파이썬 버전을 사용할려면, 프로젝트 루트 경로에서 아래 명령을 수행
# .python-version 파일이 생성됩니다. 디렉토리를 벗어나면 global 버전을 따릅니다.
# 물론 지정된 파이썬 버전은 먼저 설치되어있어야 합니다.
pyenv install 3.10.6
pyenv local 3.10.6