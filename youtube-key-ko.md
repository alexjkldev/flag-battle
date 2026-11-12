# Flag Battle: 내 YouTube API 키 만들기

스트리머 모드는 YouTube Data API를 통해 라이브 방송의 채팅을 읽습니다. 키가 없으면 하루 5분 체험만 가능하지만, 무료 개인 키가 있으면 몇 시간이고 방송할 수 있습니다. 약 5분이면 됩니다.

## 1. Google Cloud 열기

[console.cloud.google.com](https://console.cloud.google.com/)에 접속해 아무 Google 계정으로 로그인합니다(채널 계정이 아니어도 됩니다). 요청하면 약관에 동의하세요. 신용카드는 필요 없습니다.

## 2. 프로젝트 만들기

페이지 상단의 프로젝트 선택(**Select a project**)을 클릭한 다음 **New project**를 클릭합니다. 이름은 아무거나 괜찮습니다(예: `flag-battle`). **Create**를 클릭하고 상단에서 새 프로젝트가 선택되어 있는지 확인합니다.

## 3. YouTube Data API 사용 설정

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)를 열고 **Enable**을 클릭합니다.

## 4. 키 만들기

[Credentials](https://console.cloud.google.com/apis/credentials)를 열고 **Create credentials** → **API key**를 클릭합니다. 새 키를 열어 수정합니다.

- **API restrictions** → **Restrict key** → **YouTube Data API v3**만 선택합니다. 그러면 키가 유출되어도 다른 용도로는 쓸 수 없습니다.
- **Application restrictions**는 **None**으로 두어도 됩니다.

**Save**를 클릭한 다음 키를 복사합니다(**Show key** → 복사).

## 5. 앱에 붙여넣기

Flag Battle에서 **설정 → 결투 → 스트리머 모드**를 열고 YouTube API 키 칸 옆의 붙여넣기 버튼을 탭합니다. 키는 휴대전화의 보안 저장소에만 저장되며 화면에는 절대 표시되지 않습니다.

## 알아두면 좋은 점

- **무료입니다.** 기본 할당량은 하루 10,000단위입니다. 채팅을 8초마다 읽으면 하루 약 4.4시간 방송할 수 있습니다(5초마다 ≈ 2.8시간, 10초마다 ≈ 5.6시간). 간격은 앱에서 선택할 수 있습니다.
- **할당량은 태평양 시간 자정에 초기화됩니다.** 다 쓰면 앱의 **다음** 블록에 표시되고, 대결은 무작위 국기로 계속됩니다.
- 다른 곳에서 할당량을 쓰지 않도록 이 프로젝트는 Flag Battle 전용으로 사용하세요.
- 키를 취소하려면 [Credentials](https://console.cloud.google.com/apis/credentials)에서 삭제하세요.
