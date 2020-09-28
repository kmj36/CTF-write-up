# 문제 정보
1. 문제 링크: [Link](https://ctf.j0n9hyun.xyz/challenges#Terrorist)
2. 문제 푼 날짜: 2020-09-23
3. 분류: Forensics
4. 문제 이름: Terrorist

# 문제 푼 과정

포렌식 문제 중 특이한 문제인 'Terrorist'를 풀어 보겠다.

![main](D:\git 관련\CTF-write-up\HackCTF\Forensics\Terrorist\pic\main.PNG)

문제를 보면 먼저 Artifact.7z 라는 압축파일이 보인다.



또

![files](D:\git 관련\CTF-write-up\HackCTF\Forensics\Terrorist\pic\files.PNG)

압축파일은 열릴 수 있게 되어 있으며 이미지는 고장나 있다.

이미지에 문제가 생긴 것을 보니 이미지 파일에 단서가 있다는 것 같다.

![hxd](D:\git 관련\CTF-write-up\HackCTF\Forensics\Terrorist\pic\hxd.PNG)

HxD로 열어 보니 jpg의 파일 시그니처가 아닌 m4a 라는 음성 파일 시그니처인 것이 보인다.

![m4a](D:\git 관련\CTF-write-up\HackCTF\Forensics\Terrorist\pic\m4a.PNG)

파일의 확장자를 .m4a 로 바꾸어 보았다.

음성 파일을 들어 보니 무언가 이상한 목소리로 말하는 번역기의 목소리가 들린다.

자세히 들어보니 음성이 특이하게 시작 부분이 높고 끝 부분이 작다.

음성이 거꾸로 되어 있는 것 같다.

거꾸로 한 음성![davinch](D:\git 관련\CTF-write-up\HackCTF\Forensics\Terrorist\pic\davinch.PNG)

은 다음과 같이 들린다.



나레이션:

미션을 수행하는 요원들에게 알립니다. 다음 테러 목표지점은 ''서울남산타워'' 입니다.

HackCTF{서울남산타워}