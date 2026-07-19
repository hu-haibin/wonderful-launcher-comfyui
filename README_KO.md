🌐 [English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH_TW.md) | [日本語](README_JA.md) | **한국어**

<div align="center">

# Wonderful Launcher for ComfyUI on Windows

### ComfyUI 워크플로를 내려받았다면, 이제 실제로 실행되게 만드세요.

[**2.1.11 다운로드**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**공식 웹사이트**](https://wonderfullauncher.com/) · [**문서**](https://wonderfullauncher.com/docs) · [**문제 제보**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 다운로드

- **권장 다운로드**: [Wonderful Launcher 2.1.11 Setup](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **설치 파일**: `WonderfulLauncher-Setup-v2.1.11.exe`
- **체크섬 파일**: 같은 Release의 `SHA256SUMS.txt`
- **이전 안정 버전**: [2.1.10](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10)

> [!WARNING]
> GitHub가 자동으로 생성한 `Source code.zip` 또는 `Source code.tar.gz`를 다운로드하지 마세요. 이것들은 소스 압축 파일이며 Windows 설치 파일이 아닙니다.

> [!TIP]
> 일반 설치 파일은 필요한 데스크톱 실행 환경을 포함합니다. Microsoft .NET Desktop Runtime을 따로 설치할 필요가 없습니다.

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher home screen" width="86%" />
</p>

---

## 어떤 문제를 해결하나요?

ComfyUI 워크플로가 누락된 모델, 빨간 노드, 누락된 의존성, 시작 오류 때문에 멈출 때 Wonderful Launcher는 필요한 복구 단계를 현재 사용하는 ComfyUI 패키지 옆에 모아 줍니다.

| 상황 | Wonderful Launcher가 도와주는 일 |
|------|-----------------------------------|
| 이미 ComfyUI가 있음 | 기존 ComfyUI 또는 portable ComfyUI 폴더 가져오기 |
| 깨끗한 환경이 필요함 | 새 ComfyUI 패키지 배포 |
| ComfyUI가 시작되지 않음 | 시작 로그 확인 및 승인된 복구 작업 실행 |
| 워크플로에 모델이 없음 | 모델 이름 매칭 후 필요한 위치에 다운로드 또는 배치 |
| 워크플로에 노드가 없음 | 누락된 custom node와 의존성 설치 |
| 여러 ComfyUI가 하나의 모델 폴더를 공유해야 함 | 공유 모델 디렉터리 설정 |

## 2.1.11 변경 사항

- Torch 사전 탐지가 시간 초과되었다는 이유만으로 오해를 부르는 복구 창을 띄우지 않습니다.
- 누락된 모델 처리는 실행 중인 ComfyUI WebView 작업 공간에서 진행됩니다.
- 모델 결과 목록은 모델 이름, 대상 폴더, 매칭 상태, 다운로드 동작에 집중합니다.
- 공유 모델 폴더 설정은 더 명확한 A → B 구조로 표시됩니다.
- 이미지 생성 대화의 prompt를 더 자연스럽게 선택하고 복사할 수 있습니다.

## 빠른 시작

1. [최신 Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)를 엽니다.
2. `WonderfulLauncher-Setup-v2.1.11.exe`를 다운로드합니다.
3. 설치 후 기존 ComfyUI를 가져오거나 새 ComfyUI 패키지를 배포합니다.
4. 워크플로에 모델이나 노드가 없으면 알림 표시줄의 안내에 따라 매칭, 다운로드 또는 복구를 진행합니다.

이 저장소는 Windows 설치 파일, 스크린샷, 이슈 추적을 위한 공개 페이지입니다. 데스크톱 앱의 전체 공개 소스코드 미러가 아닙니다.
