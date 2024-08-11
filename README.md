# ADP_Study

1. 스터디 목적 : 10/12 제 33회 ADP 실기 전원 합격 스터디
2. 스터디 시간 : 매주 토요일, 05:00~09:00 (모의테스트)
3. 스터디 장소 : GOOGLE MEET
4. 스터디 운영계획 (2024년 8월 ~ 10월)
- 2024년 8월 17일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 8월 24일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 8월 31일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 9월 7일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 9월 14일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 9월 21일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 9월 28일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)
- 2024년 10월 5일 : 출제자 TBD, 모의테스트 (05:00 ~ 09:00)

5. 스터디운영방법 : 매주 토요일 모의테스트 진행
                  필요 시, 주중 스터디 보완진행
- 부교재 
	+ 매주 테스트문제 출제 : 매주 출제자 변경
- 주교재 
	+ (교재1)[통계학:파이썬을 이용한분석](https://ridibooks.com/books/754039038?_s=search&_q=%ED%86%B5%EA%B3%84%ED%95%99%3A%ED%8C%8C%EC%9D%B4%EC%8D%AC%EC%9D%84+%EC%9D%B4%EC%9A%A9%ED%95%9C%EB%B6%84%EC%84%9D&_rdt_sid=search&_rdt_idx=0)
	+ (교재2)[데이터마님실기문제](https://www.datamanim.com/dataset/ADPpb/index.html)
	+ [ADP 자료 모음](https://github.com/jeong-wooseok/ADPfork)


윈도우즈 powershell 기준으로 (ananconda prompt) 설명드립니다.
```powershell
git clone git@github.com:jeong-wooseok/ADP_Study.git
```
깃허브를 복사합니다. 클론이 안되면 SSH 연결이 안되었을 수도 있습니다.

```powershell
Copydir $env:USERPROFILE\.ssh
```
ssh를 복사합니다.
만약 .ssh 폴더가 없거나 비어있다면, SSH 키를 생성해야 합니다. Windows에서 SSH 키를 생성하고 GitHub에 추가하는 과정은 다음과 같습니다:

SSH 키 생성:
```powershell
Copyssh-keygen -t ed25519 -C "your_email@example.com"
```
기본 위치와 파일 이름을 사용하려면 그냥 Enter를 누르세요


SSH 에이전트 시작:
```powershell
CopyStart-Service ssh-agent
```

SSH 키를 에이전트에 추가:
```powershell
Copyssh-add $env:USERPROFILE\.ssh\id_ed25519
```

공개 키 복사:
```powershell
CopyGet-Content $env:USERPROFILE\.ssh\id_ed25519.pub | clip
```
GitHub에 SSH 키 추가:

GitHub.com에 로그인
오른쪽 상단의 프로필 아이콘 클릭 -> Settings
왼쪽 사이드바에서 "SSH and GPG keys" 클릭
"New SSH key" 또는 "Add SSH key" 클릭
제목 입력 (예: "My Windows PC")
키 필드에 클립보드의 내용 붙여넣기
"Add SSH key" 클릭


GitHub 연결 테스트:
```powershell
Copyssh -T git@github.com
```

저장소 클론 재시도:
```powershell
Copygit clone git@github.com:jeong-wooseok/ADP_Study.git
```

이 과정을 따라해보시고, 여전히 문제가 있다면 알려주세요. 추가적인 도움을 드리겠습니다.
