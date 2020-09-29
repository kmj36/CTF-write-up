# 문제 정보
1. 문제 링크: [Link](https://ctf.j0n9hyun.xyz/challenges#Smooth%20CipherText)
2. 문제 푼 날짜: 2020-09-24
3. 분류: Cryptography
4. 문제 이름: Smooth CipherText

# 문제 푼 과정

암호 문제인 'Smooth CipherText'를 풀어 보았다.

![main](D:\git 관련\CTF-write-up\HackCTF\Cryptography\Smooth CipherText\pic\main.PNG)

문제를 열면 먼저 암호화된 텍스트가 보인다.

암호화 방식 중 일단 2진수 처럼 못 알아보는 텍스트가 아니니

비즈네르, 카이사르 같은 옛날 암호화 방식인 것 같다.



일단 끝 부분에 LymoADJ = HackCTF 인것 같다.

일단 카이사르인지 판별해 보자.

CTF

ADJ(-2, -14, -4)로 일치 하지 않는다. 즉 카이사르는 아닌 것으로 보인다.



일단 비즈네르로 복호화하니 키 'keykey' 에서 정확하게 복호화된 암호문을 찾을 수 있었다.![decode](D:\git 관련\CTF-write-up\HackCTF\Cryptography\Smooth CipherText\pic\decode.PNG)

해독한 문장은 '아아아아안녕하세요 모두들! 당신은 제가 누군지 아시나요? 제 이름은 Smoothman 어... 저는 당신이 원하는 것을 아주 잘 알고 있습니다! 만약 당신이 이 암호문을 복호화 할수 있다면, 당신은 올바른 답을 얻을 수 있습니다. 그래서, 플래그는 Hackctf{flag} 입니다.'라고 적여 있다.



그런데 플래그가 정상적으로 출력되지 않았다.

한번더 돌려 보니 키 'nn' 에서 

![decode2](D:\git 관련\CTF-write-up\HackCTF\Cryptography\Smooth CipherText\pic\decode2.PNG)


정상적인 플래그가 나왔다.

'나는 너를 기억할 것이다. 그러므로, 나를 잊지 말아라.'