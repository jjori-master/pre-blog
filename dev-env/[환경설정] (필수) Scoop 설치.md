#### [환경설정] (필수) Scoop 설치

> https://scoop.sh/
> https://github.com/ScoopInstaller/Awesome
>
> PowerShell Core 설치 및 닷넷 프레임워크 4.5 이상
> 유저 Home 경로에 설치하기에 관리자 권한을 요구하지 않습니다.

```bash
# 파워쉘에서 scoop 설치
iwr -useb get.scoop.sh | iex
# 최초 필수 설치
scoop install git

# add buckets
# 간혹 기본 설치된 버킷 버전이 낮아 업데이트 오류가 발생 할 수 있기에, 삭제 후 다시 추가
scoop bucket rm main 
scoop bucket add main
scoop bucket add extras
scoop bucket add nerd-fonts

# update scoop
# "update of date" 메시지가 출력되면 soop update를 합니다.
scoop status
scoop update
```

```bash

```









