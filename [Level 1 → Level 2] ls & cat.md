[<img width="776" height="448" alt="image" src="https://github.com/user-attachments/assets/2829bb20-f244-43ab-8bd9-185846a356e7" />](https://overthewire.org/wargames/bandit/bandit2.html)
-라는 파일에 bandit2의 비밀번호가 있으니 찾아서 읽으라는 문제다.

<img width="608" height="58" alt="image" src="https://github.com/user-attachments/assets/a715911b-382b-43f5-9275-808de1c3f5ca" />
- 라는 파일 제목으로 그냥 ls로 찾으면 나오지 않는다. 하지만 ls -l로 찾으면 나온다.

이는 `ls -` 이라고 작성하면 쉘은 -를 파일이름이 아니라 **옵션** 으로 인식하기 때문에 결과가 나오지 않는다. 딱히 숨겨진 파일은 아니기 때문에 옵션을 붙여 -를 찾으니 나왔다. 만일 숨겨진 파일이었다면 `-l` 옵션으로는 발견하지 못한다. `-a` 옵션을 사용해 찾아야한다.

```bandit1@bandit:~$ cat < -```

위와 같이 `<`를 작성하여 입력하면 -와 같은 dashed filename도 읽어올 수 있다.

# ls 옵션
<img width="882" height="368" alt="image" src="https://github.com/user-attachments/assets/77ce1215-7cb6-430c-bae1-c92a596ff410" />
> Gemini

# cat 옵션
<img width="882" height="457" alt="image" src="https://github.com/user-attachments/assets/4260ba87-9348-4bbc-a6de-5ae1b60c775b" />

## cat 옵션 about 특수 파일 이름
<img width="877" height="304" alt="image" src="https://github.com/user-attachments/assets/06048b84-d1de-495f-ad6c-36a8a447aaf6" />

> Gemini

<img width="904" height="579" alt="image" src="https://github.com/user-attachments/assets/b304b617-1ac9-44cd-a53d-d71aac7aa2a3" />
성공~
