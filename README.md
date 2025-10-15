# Bandit 문제 풀이 정리
목적: **리눅스 기본기** 를 더 단단히 다지기 위해

환경: **Linux** (Ubuntu)

기타: Try Hack Me 보다는 간결하게 정리하고, 주로 리눅스 명령어를 공부할 예정

꿀팁:
Bandit 문제를 풀 때마다 발견하는 **비밀번호** 를 꼭 local host에 저장해둬야 한다. 이때 **gedit** 으로 저장한 뒤, 그대로 텍스트 편집기에서 복붙하면 **비밀번호가 틀린다.**

이유는 텍스트 편집기에서 쉘로 복붙하면 **보이지 않는 문자** 때문이다. 예를 들면 \n 같은 공백 문자 등 말이다

따라서 **gedit** 으로 저장했어도 **shell** 에서 따로 **cat** 으로 읽은 뒤 쉘에서 쉘로 복붙해야한다.

[<img width="248" height="97" alt="image" src="https://github.com/user-attachments/assets/d81a77eb-6c8e-4ae5-9a32-5e810f1ff400" />](https://overthewire.org/wargames/bandit/bandit0.html) [<img width="459" height="90" alt="image" src="https://github.com/user-attachments/assets/33ad4eb3-d416-4337-b389-e7933c505fef" />](https://overthewire.org/wargames/bandit/bandit0.html)
