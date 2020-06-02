#### [환경설정] (필수) WSL 설치

> [Windows 10에 Linux용 Windows 하위 시스템 설치 가이드](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10)
>
> 현재 WSL2가 나왔지만 우선 WSL만 설치하고 공부를 하고 나중에 업그레이드 한다.
>
> 흉내쟁이님의 [[윈도우즈에서 리눅스 설치 - WSL](https://webdir.tistory.com/541)](https://webdir.tistory.com/541)를 거의 베끼다시피 했다. 우선 빨리 설치하고 다음으로 넘어가자



###### Phase01.  윈도우 최신 버전 업데이트

> 설정 > 업데이트 및 보안 에서 최신 버전으로 업데이트 한다.
>
> 최신버전으로 업데이트 하면 WSL을 사용할 수 있다. 



###### Phase02.  Windows 기능 켜기/끄기에서 `Linux용 Windows 하위 시스템` 을 체크한다.

> 또는 PowerShell을 띄우고 아래 명령어를 실행해도 된다.

```powershell
$> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```



###### Phase03. Microsoft Store로 이동하여 Ubunut로 검색하여 다운로드 실행한다.

> 현재 시점 기준(2020.06.03) Ubuntu 20.04 LTS 버전을 설치하였다.



###### Phase04.  리눅스 기본 계정을 설정한다.