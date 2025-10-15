[<img width="856" height="573" alt="image" src="https://github.com/user-attachments/assets/70c9bdfe-f24c-4cd3-ab5f-40a595c39bb7" />
](https://overthewire.org/wargames/bandit/bandit0.html)

SSH 포트로 접속하라는 문제이다. 문제에서 Host와 계정, 포트 번호와 비밀번호를 모두 주어줬다.

문제를 풀기에 앞서, SSH란 무엇인가 간단하게 알아보겠다.

# SSH란?
> **Secure Shell Protocol** (SSH Protocol)은 네트워크 상의 다른 컴퓨터에 로그인하거나 **원격 시스템** 에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 해 주는 **응용 프로그램** 또는 그 **프로토콜** 이다.
>
> 기본적으로 **22번** 포트를 사용한다.
>
> SSH는 **암호화** 기법을 사용하기 때문에 통신이 노출된다고 하더라도 이해할 수 없는 암호화된 문자로 보인다.
>
> _Wiki_

마지막 인용글을 보면 **VPN** 이 떠오르기도 한다.

구글에 SSH와 VPN의 차이를 검색하면 AI가 아래 캡처와 같이 정리를 해준다.

# SSH와 VPN 차이
<img width="826" height="479" alt="image" src="https://github.com/user-attachments/assets/e788ae82-d8bc-418c-866a-cfa7794daeb1" />

우선 가장 큰 차이점은 작동 Level이다. SSH는 애플리케이션층에서, VPN은 운영체제 수준에서 작동한다.

Try Hack Me의 경우에는 `VPN`을 활용해 **가상 네트워크** 에 접속하여, **Victim IP** 를 가진 **VM** 을 공격하는 방식으로 문제를 풀 수 있다.

Bandit은 `SSH`를 활용해 이미 만들어진 서버에 특정 사용자 계정으로 접속하는 방식이다. 즉, 모의해킹이 아닌 `해당 시스템에 접속 권한을 가진 사용자 입장`에서 탐색하며 푸는 **War Game** 이다.

이제 이어서 Linux에서 사용하는 `SSH 명령어`를 알아보도록 하겠다.

# ```ssh 계정@IP```

#### `-4/6` : IPv4 혹은 IPv6로만 접속하도록 한다.
#### `-C` : 모든 데이터를 압축하여 전송한다.
#### `-E log_file` : log_file 에 이어서 디버그 로그를 기록한다.
#### `-p port` : remote host에 대한 포트로 접속한다.
#### `-q` : 조용한 모드, 대부분의 경고나 메세지를 보이지 않게 한다.
#### `-i identity_file` : 공개 키 인증 방식에서 사용할 개인 키(private key) 파일의 경로를 지정한다.

이외의 더 많은 옵션이나 설명은 ```man 명령어``` 를 통해 특정 명령어에 대한 설명을 알 수 있다.

<br>

따라서, 문제에서 계정, ip, 포트 넘버를 알려줬기에 아래와 같이 작성하면 Bandit 0에 접속할 수 있다.

```seed@VM:~$ ssh bandit0@bandit.labs.overthewire.org -p 2220```

<img width="489" height="144" alt="image" src="https://github.com/user-attachments/assets/3798f979-62ef-44b0-a4c2-9839ba49c817" />

앞으로 이와 같은 방식으로 Bandit 문제들을 풀 수 있다.
