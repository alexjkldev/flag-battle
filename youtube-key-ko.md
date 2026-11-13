# Flag Battle: 내 YouTube API 키 만들기

스트리머 모드는 YouTube Data API를 통해 라이브 방송의 채팅을 읽습니다. 키가 없으면 하루 5분 체험만 가능하지만, 무료 개인 키가 있으면 몇 시간이고 방송할 수 있습니다. 약 5분이면 됩니다.

## 1. Google Cloud 열기

[console.cloud.google.com](https://console.cloud.google.com/)에 접속해 아무 Google 계정으로 로그인합니다(채널 계정이 아니어도 됩니다). 요청하면 약관에 동의하세요. 신용카드는 필요 없습니다.

## 2. 프로젝트 만들기

페이지 상단의 프로젝트 선택(**Select a project**)을 클릭한 다음 **New project**를 누르세요. 이름은 아무거나 괜찮아요(예: `flag-battle`). **Create**를 누르고 상단에 새 프로젝트가 선택됐는지 확인하세요. 이후 작업은 모두 이 프로젝트에서 합니다.

## 3. YouTube Data API v3 사용 설정 — 키를 만들기 전에

[YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com)를 열고 **Enable**을 누르세요. 버튼이 **Manage**로 바뀌면 켜진 거예요. 이 단계를 건너뛰면 키가 작동하지 않아요.

## 4. 키 만들기

[Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. API 제한 목록에서 **YouTube Data API v3**만 선택하고 **Create**를 누르세요. **API key created** 창에 키가 표시되면 복사하세요.

목록에 YouTube Data API v3가 없으면 3단계로 돌아가세요. 애플리케이션 제한은 **None**으로 두세요.

## 5. 앱에 붙여 넣기

Flag Battle에서: 메인 화면 → **설정** → 모드 **듀얼** → **스트리머 모드** → **켜기**. **내 YouTube API v3 키** 옆의 붙여 넣기 버튼을 누르세요(아래 힌트 문구 칸이 아니에요). 키는 휴대폰의 보안 저장소에만 저장되며 화면에 표시되지 않아요.

## 키가 거부되면

이유는 **다음** 블록에 표시돼요:

- **「이 키에 YouTube Data API v3가 꺼져 있어요」** — 키가 있는 같은 프로젝트에서 3단계를 하고 몇 분 기다리세요.
- **「키 제한이 YouTube를 막고 있어요」** — [Credentials](https://console.cloud.google.com/apis/credentials)에서 키를 열고 API 제한에 **YouTube Data API v3**가 있는지, 애플리케이션 제한이 **None**인지 확인하세요.
- **「YouTube 키가 올바르지 않아요」** — 키가 덜 복사됐어요. 키는 `AIza`로 시작하는 39자예요.

고친 뒤 메뉴로 돌아가 방송을 다시 시작하세요.

## 알아두면 좋은 점

- **무료입니다.** 기본 할당량은 하루 10,000단위입니다. '즉시' 모드에서는 채팅이 실시간으로 도착하며 하루 약 6시간 방송할 수 있습니다. '절약' 모드는 최대 10초 지연 대신 약 12시간까지 늘려 줍니다. 모드는 앱에서 선택할 수 있습니다.
- **할당량은 태평양 시간 자정에 초기화됩니다.** 다 쓰면 앱의 **다음** 블록에 표시되고, 대결은 무작위 국기로 계속됩니다.
- 다른 곳에서 할당량을 쓰지 않도록 이 프로젝트는 Flag Battle 전용으로 사용하세요.
- 키를 취소하려면 [Credentials](https://console.cloud.google.com/apis/credentials)에서 삭제하세요.
