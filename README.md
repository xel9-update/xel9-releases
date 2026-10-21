# XEL9 releases

XEL9 앱의 **공식 배포 저장소**입니다. 1Pixel Inc.가 만든 XEL9 앱의 설치 파일과 자동 업데이트 파일을 여기서 내려받습니다.
소스 코드는 이 저장소에 없습니다. 파일은 각 앱의 빌드가 서명한 뒤 자동으로 올립니다.

This is the **official download repository** for the XEL9 apps by 1Pixel Inc.: installers and auto-update packages, published automatically by each app's build. No source code is kept here.

- 홈페이지 / Website: https://www.xel9.com
- 릴리즈 목록 / All releases: [Releases](../../releases)

## 앱 / Apps

| 앱 | 릴리즈 태그 | 설명 |
|---|---|---|
| **XEL9-Z** | `vX.Y.Z` (예: `v0.5.1`) | 암호화 보관함·압축 프로그램 (Windows, macOS) |
| **XEL9-C** | `XEL9-C-vX.Y.Z` (예: `XEL9-C-v0.2.0`) | 보안 중심 PC 정리·최적화 도구 (Windows, macOS) |

다른 XEL9 앱은 `<앱 이름>-vX.Y.Z` 형식의 태그로 이 목록에 더해집니다.

## 내려받기 / Download

각 릴리즈의 **Assets**에서 운영체제에 맞는 파일을 받습니다. XEL9-Z 설치 파일은 버전 없는 이름으로도 올라가 있어, 아래 링크는 항상 XEL9-Z 최신판을 줍니다.
XEL9-C는 `XEL9-C-v…` 릴리즈의 Assets에서 받습니다(파일 이름이 `XEL9-C_…`로 시작).

| 운영체제 | 파일 | 최신판 링크 |
|---|---|---|
| Windows 10/11 (x64) | 설치 프로그램 `.exe` (권장), `.msi` | [XEL9-Z_x64-setup.exe](../../releases/latest/download/XEL9-Z_x64-setup.exe) |
| macOS 11 이상 (Apple Silicon·Intel) | `.dmg` | [XEL9-Z_universal.dmg](../../releases/latest/download/XEL9-Z_universal.dmg) |
| 명령줄 도구 (CLI) | `xel9-z-cli-*.zip` / `.tar.gz` | 릴리즈의 Assets |

## 업데이트 / Updating

### 자동 업데이트

앱의 **설정 → 업데이트**에서 확인하거나 "앱을 시작할 때 업데이트 확인"을 켜 두면, 앱이 새 버전을 알려 주고 받아서 설치합니다.
업데이트 파일은 앱에 들어 있는 공개 키로 서명을 확인하며, 맞지 않으면 설치하지 않습니다.

### 직접 받아서 업데이트하기

자동 업데이트를 쓰지 않거나 실패했을 때는 최신 설치 파일을 받아 **기존 앱 위에 설치**하면 됩니다. 설정, 우클릭 메뉴, 신뢰 목록, 보관함은 그대로 남습니다.

1. 위 표나 [최신 릴리즈](../../releases/latest)에서 운영체제에 맞는 파일을 받습니다.
2. (권장) 같은 릴리즈의 `SHA256SUMS`로 파일이 온전한지 확인합니다.
   - macOS: `shasum -a 256 -c SHA256SUMS --ignore-missing`
   - Windows (PowerShell): `Get-FileHash .\XEL9-Z_0.5.1_x64-setup.exe -Algorithm SHA256` 결과를 `SHA256SUMS`의 같은 이름 줄과 비교
3. 운영체제별로 설치합니다.
   - **Windows:** 앱을 닫고 받은 `-setup.exe`를 실행합니다. 같은 위치에 덮어 설치됩니다(`.msi`로 설치했다면 새 `.msi`를 실행).
   - **macOS:** 앱을 종료하고 `.dmg`를 열어 앱을 **응용 프로그램** 폴더로 끌어다 놓은 뒤 "대치"를 고릅니다.
4. 앱을 다시 열어 **설정 → 정보**에서 버전을 확인합니다.

릴리즈에는 앱이 자동 업데이트에 쓰는 파일(`*.app.tar.gz`, `*-setup.exe`)도 함께 있습니다. 직접 설치할 때는 위 표의 설치 파일을 쓰면 됩니다.

### 안전하게 받기

- XEL9 앱은 **이 저장소와 https://www.xel9.com 에서만** 받으세요. 다른 곳에서 받은 파일은 실행하지 마세요.
- macOS 앱은 Apple Developer ID로 서명하고 공증(notarization)을 받았습니다.
- Windows에서 처음 실행할 때 SmartScreen이 경고하면, 이 저장소나 홈페이지에서 받은 파일인지 확인한 뒤 "추가 정보 → 실행"을 누릅니다.
- 보안 문제를 발견하면 홈페이지의 연락처로 알려 주세요.

## 저작권 / Copyright

© 2026 XEL9 by 1Pixel Inc. All Rights Reserved.

XEL9 앱은 1Pixel Inc.의 비공개(proprietary) 소프트웨어입니다. 이 저장소의 파일은 개인과 조직이 해당 앱을 설치·업데이트하는 용도로 배포됩니다. 1Pixel Inc.의 허락 없이 수정하거나, 다른 곳에 다시 배포하거나, 판매할 수 없습니다.
앱에 쓰인 오픈소스 구성 요소의 라이선스는 앱의 **설정 → 정보 → 오픈소스 라이선스**와 설치 폴더의 `THIRD_PARTY_NOTICES.md`에 있습니다.

XEL9 apps are proprietary software of 1Pixel Inc. The files here are provided for installing and updating the apps; modifying, redistributing or selling them without permission is not allowed. Open-source components are listed in each app (Settings → About → Open-source licenses) and in `THIRD_PARTY_NOTICES.md` in the installation folder.
