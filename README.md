# ZM GameChat Translator

게임 화면의 영어·중국어 채팅을 읽고 **한국어 번역을 화면 위에 표시**하는 Windows 앱입니다.

- 기본 구글 무료 번역: 계정·API 키 없이 시작
- 내장 OCR: Windows 언어팩 별도 설치 불필요
- 한국어 채팅 보완, 게임별 용어집, 위치를 조절할 수 있는 번역창
- WarDogs 채널과 팀 색상 지원
- 로그 기록은 기본 비활성화

## 다운로드

**현재 첫 GitHub 배포본을 준비 중입니다.** 게시된 파일이 아직 없다면 전달받은 테스트 ZIP을 사용하세요.

[배포 파일 보기](https://github.com/ZM-kr/ZM_gamechat_translator-releases/releases)

릴리스가 게시되면 **Assets**에서 `ZM-GameChatTranslator-…-win-x64.zip`을 받으세요. `Source code` ZIP은 이 안내 문서의 사본이며 프로그램이 아닙니다. `SHA256SUMS.txt`는 다운로드한 ZIP의 손상 여부를 확인하는 데 사용합니다.

Windows x64용이며 .NET 런타임과 OCR 모델이 포함됩니다. 최소 대상은 Windows 10 2004 이상이고 현재 검증 환경은 Windows 11입니다.

## 시작하기

1. ZIP을 모두 풀고 `ZM.GameChatTranslator.exe`를 실행합니다. 실행 파일 옆의 **models 폴더**를 함께 보관하세요.
2. 설정 마법사에서 기본 **구글 무료 번역**으로 연결을 확인합니다. 인터넷 연결이 필요합니다.
3. 게임을 창 모드 또는 테두리 없는 창 모드로 열고 채팅 영역을 지정합니다.
4. 번역창 위치를 정하고 **저장·적용 → 번역 시작**을 누릅니다. 기본 단축키는 **Ctrl+Alt+T**입니다.

[처음 실행 안내](START-HERE.txt) · [상세 설정](docs/TESTER-GUIDE.md) · [변경 사항](docs/RELEASE-NOTES.md)

<details>
<summary>스마트 앱 컨트롤(SAC)로 실행이 차단될 때</summary>

테스트판은 코드 서명이 없어 Windows가 실행을 차단할 수 있습니다. 받은 파일과 배포자를 신뢰하고 설정 변경에 동의한다면 **Windows 보안 → 앱 및 브라우저 컨트롤 → 스마트 앱 컨트롤 설정 → 끄기**를 선택한 뒤 다시 실행할 수 있습니다.

이 앱만 허용하는 기능은 없으며 **PC 전체의 SAC 보호가 꺼집니다.** Defender 실시간 보호는 켜 두세요. 최신 Windows 업데이트에서는 SAC를 다시 켤 수 있지만 이전 버전은 Windows 초기화·재설치가 필요할 수 있습니다. 변경 전 업데이트와 설정 화면의 안내를 확인하세요. 다시 켜면 앱이 재차 차단될 수 있습니다.

설정 변경은 선택 사항입니다. 변경을 원하지 않으면 차단 문구를 제보해 주세요. [Microsoft 공식 FAQ](https://support.microsoft.com/en-us/windows/security/threat-malware-protection/smart-app-control-frequently-asked-questions)

</details>

## 사용 시 알아둘 점

- 번역 중에는 지정한 화면 영역을 계속 읽습니다. 다른 앱이 그 자리를 덮으면 해당 글자도 번역될 수 있으므로 게임을 하지 않을 때는 번역을 중지하세요.
- 화면 이미지는 로컬에서 처리하고, 번역에 필요한 텍스트는 선택한 번역 서비스로 전송합니다. 로그는 기본으로 꺼져 있고 자동 전송하지 않습니다.
- 작은 글자·빠른 스크롤·복잡한 배경에서 OCR 오인식이 생길 수 있습니다. 번역 속도와 품질은 서비스에 따라 달라집니다.
- 구글 무료 번역은 비공식 연결 방식으로 제한이나 중단이 있을 수 있습니다.
- 게임별 외부 도구 사용 정책을 확인하세요. 모든 게임과의 호환성을 보장하지 않습니다.

## 문제 제보

[Issues에서 제보하기](https://github.com/ZM-kr/ZM_gamechat_translator-releases/issues/new/choose)

앱 버전, Windows 버전, 게임, 증상과 재현 순서를 알려 주세요. **Issues는 공개됩니다.** API 키·계정 정보·개인 대화·설정 파일·원본 로그는 올리지 마세요. 화면을 첨부할 때도 개인정보를 가려 주세요.

## 라이선스

이 저장소는 배포 파일과 사용자 안내를 제공합니다. 앱 소스와 개발 작업 기록은 포함하지 않습니다. [MIT 라이선스](LICENSE)와 [제3자 고지](THIRD_PARTY_NOTICES.md)를 확인하세요. 배포 ZIP에도 해당 라이선스와 고지가 포함됩니다.
