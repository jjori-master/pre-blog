#### [개발환경] (필수) pyenv로 python 환경설정

> [Install Python 3.7.4 in pyenv on Ubuntu 18.04](https://mahdiech.com/install-python-374-in-pyenv-on-ubuntu-1804/)을 거의 대부분 차용하였음.



##### Phase01. WSL에 pyenv 설치전 필요 라이브러리 설치

```bash
# install pyenv requment libraries
sudo apt-get install \
    build-essential \
    libsqlite3-dev \
    sqlite3 \
    bzip2 \
    libbz2-dev \
    zlib1g-dev \
    libssl-dev \
    openssl \
    libgdbm-dev \
    libgdbm-compat-dev \
    liblzma-dev \
    libreadline-dev \
    libncursesw5-dev \
    libffi-dev \
    uuid-dev
```



###### Phase02. pyenv 설치

```bash
# install pyenv
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
```



###### Phase03. Shell 재실행 및 pyenv 설치 확인

```bash
$> exec $SHELL
$> pyenv -v
pyenv 1.2.18-19-gcf81e5a0 -> 버전이 나오면 정상 설치
```



###### Phase04. 사용하고자하는 Python  버전 설치

> [장고와 어떤 파이썬 버전을 사용해야 하나요?](https://docs.djangoproject.com/ko/3.0/faq/install/#what-python-version-can-i-use-with-django)를 참조하면 3.0대의 Django를 사용하기위해서는
>
> 파이썬 3.6 버전이상이 필요하고 현재 나와있는 최신 버전인 3.8버전을 pyenv를 통해 설치한다.

```bash
# you can check available versions
pyenv install --list

# install python
pyenv install 3.8.2

# set default version
pyenv global 3.8.2

# check using python version
pyenv versions

# or
python — version
```

