# 문제 정보
1. 문제 링크: [Link](http://ctf.j0n9hyun.xyz:2023)
2. 문제 푼 날짜: 2020-08-23
3. 분류: Web
4. 문제 이름: Hidden

# 문제 푼 과정
![menu](/pic/link_menu.PNG)

CTF에 있는 web Hidden 문제를 선택하니 링크가 나왔다.
링크를 타고 들어가면

![main](/pic/main.PNG)

이렇게 생긴 웹이 떳다. 그런데 이 사이트에 이상한 점은
"5번 파일에 플래그가 있다악!!!!!!!!!!!" 라고 적혀있고 4번까지 밖에 버튼이 없는 걸 확인할 수 있다.

![Nop](/pic/Nop.PNG)
그리고 버튼을 누르면 'Nop'이라는 메시지가 응답한다.

![html](/pic/html.PNG)
html를 확인했더니 특이한 점이
1. 버튼 타입이 'submit'으로 서버와 전달한다.
2. HTTP 메소드가 'get'으로 서버로부터 정보를 조회한다.
3. 입력 값이 1,2,3,4가 있다.

즉 [클라이언트 숫자 값 전달 > 서버 정보 조회 > 클라이언트 메시지]로 이루어진다는 것이다.

그러므로 body에다가
```html
<form method="get">
    <input type="hidden" name="id" value="5"> //5를 전달
    <button type="submit">5</button>
</form>
```
를 삽입해보자.

![button](/pic/button.PNG)
5번째 버튼이 생성되었다.

![flag](/pic/flag.PNG)

서버에 5 값을 전달했더니 플래그가 출력되었다.