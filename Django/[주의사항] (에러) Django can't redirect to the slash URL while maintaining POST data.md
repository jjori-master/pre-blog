#### [주의사항] (에러) `Django can't redirect to the slash URL while maintaining POST data. `

> [해당 내용 풀이](http://codingdojang.com/scode/377)
> 장고의 `APPEND_SLASH`는 자동으로 URL 끝에 슬래시('/')를 붙여주는 옵션(Default=Ture)
>
> 위의 내용이 발생되는 원인은 Django가 urls.py 파일에 정의된 패턴과 일치하는 것이 없을때 자동으로 붙여서 다시 한번 일치하는지 확인하는데
>
> 일치하는 경우에는 슬래시를 붙인 url로 redirect가 일어난다.
> 문제는 POST 요청일 경우 redirct가 발생되면 submit된 데이터가 유실될 수도 있기 때문에
> 해당 오류가 발생된다.
>
> form에서 사용되는 url의 경우 끝에 슬래시('/')를 붙여준다.