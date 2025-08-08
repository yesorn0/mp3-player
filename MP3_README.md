# 🎵 MP3 플레이어

Qt Designer로 제작한 UI를 기반으로 한 MP3 플레이어 애플리케이션입니다. YouTube에서 음원을 다운로드하고 재생할 수 있습니다.

## ✨ 주요 기능

### 🎯 **기본 화면 전환**
- **시작 화면**: `lbl_music`, `btn_lyrics`, `btn_playlist`, 하단 컨트롤만 표시
- **가사 화면**: `btn_lyrics` 클릭 시 `scl_lyrics` 표시 (크기와 위치가 `lbl_music`과 동일), 다시 클릭 시 시작 화면으로 복귀
- **재생목록 화면**: `btn_playlist` 클릭 시 `scl_playlist` 표시 (크기와 위치가 `lbl_music`과 동일), 다시 클릭 시 시작 화면으로 복귀

### 📥 **YouTube 다운로드 기능**
- **다운로드 버튼**: `btn_musicdown` (pushButton) 클릭으로 YouTube 검색 및 다운로드 팝업창 열기
- **음원 검색**: 노래 제목 또는 아티스트로 YouTube 검색
- **음원 다운로드**: 선택한 음원을 MP3 형식으로 다운로드
- **자동 폴더 생성**: 다운로드 시 자동으로 `download` 폴더 생성
- **재생목록 자동 추가**: 다운로드된 음원이 재생목록에 자동 추가

### 🎵 **재생 기능**
- **재생목록 관리**: 한글, 영어, 숫자 순으로 정렬된 재생목록
- **음악 재생**: `btn_play` 클릭으로 음악 재생
- **재생 컨트롤**: 재생, 일시정지, 정지, 이전/다음 곡
- **볼륨 조절**: 볼륨 슬라이더로 음량 조절
- **진행바**: 음악 진행 상황 표시 및 탐색

## 🚀 설치 및 실행

### 1. 필요한 패키지 설치

```bash
pip install -r mp3_requirements.txt
```

### 2. UI 파일 준비

`mp3.ui` 파일이 프로젝트 폴더에 있어야 합니다.

### 3. 애플리케이션 실행

```bash
python mp3_ui_enhanced.py
```

## 📋 사용 방법

### 🎯 **기본 화면 전환**

1. **시작 화면**
   - 앱 실행 시 기본 화면
   - 음악 이미지와 기본 컨트롤만 표시

2. **가사 화면**
   - `btn_lyrics` 버튼 클릭
   - 가사 스크롤 영역 표시
   - 다시 클릭하면 시작 화면으로 복귀

3. **재생목록 화면**
   - `btn_playlist` 버튼 클릭
   - 재생목록 스크롤 영역 표시
   - 다시 클릭하면 시작 화면으로 복귀

### 📥 **YouTube 음원 다운로드**

1. **다운로드 버튼 클릭**
   - 재생목록 영역의 "다운로드" 버튼 (pushButton) 클릭
   - YouTube 검색 다이얼로그 열림

2. **음원 검색**
   - 검색창에 노래 제목 또는 아티스트 입력
   - "검색" 버튼 클릭
   - 검색 결과 리스트에 표시

3. **음원 다운로드**
   - 원하는 음원 선택 (더블클릭 또는 선택 후 "다운로드" 버튼)
   - 자동으로 `download` 폴더에 MP3 파일 저장
   - 다운로드 진행 상황 확인

4. **재생목록 자동 추가**
   - 다운로드 완료 시 자동으로 재생목록에 추가
   - 한글, 영어, 숫자 순으로 정렬

### 🎵 **음악 재생**

1. **재생목록에서 선택**
   - 재생목록 화면에서 원하는 곡 더블클릭
   - 또는 재생목록에서 곡 선택 후 `btn_play` 클릭

2. **재생 컨트롤**
   - `btn_play`: 재생/일시정지
   - `btn_pause`: 일시정지
   - `btn_stop`: 정지
   - `btn_previous`: 이전 곡
   - `btn_next`: 다음 곡

3. **볼륨 및 진행 조절**
   - `sld_volume`: 볼륨 조절
   - `sld_music`: 음악 진행 상황 표시 및 탐색

## 🛠️ 기술 스택

- **UI Framework**: PyQt5
- **미디어 재생**: QMediaPlayer
- **YouTube 다운로드**: yt-dlp
- **HTTP 요청**: requests
- **파일 처리**: mutagen

## 📁 프로젝트 구조

```
mp3-player/
├── mp3.ui                    # Qt Designer UI 파일
├── mp3_ui_enhanced.py        # 메인 애플리케이션
├── mp3_requirements.txt      # Python 패키지 의존성
├── MP3_README.md            # 프로젝트 설명서
├── playlist.json            # 재생목록 저장 파일 (자동 생성)
└── imgs/                    # 이미지 파일들 (UI에서 참조)
    ├── music.png
    ├── play.png
    ├── pause.png
    ├── stop.png
    ├── previous.png
    ├── next.png
    ├── volume_H.png
    ├── volume_L.png
    ├── volume_mute.png
    ├── shuffle.png
    ├── repeat.png
    └── repeat_1.png
```

## 🔧 주요 클래스

### MP3Player
- 메인 애플리케이션 클래스
- UI 관리 및 미디어 플레이어 제어

### YouTubeSearchDialog
- YouTube 검색 및 다운로드 다이얼로그
- 음원 검색 및 다운로드 기능

### YouTubeDownloader
- YouTube 다운로드 스레드
- 백그라운드에서 음원 다운로드 처리

## 🎨 UI 구성 요소

### 메인 화면
- `lbl_music`: 음악 이미지 라벨
- `btn_lyrics`: 가사 버튼
- `btn_playlist`: 재생목록 버튼

### 가사 화면
- `scl_lyrics`: 가사 스크롤 영역
- `lbl_lyrics`: 가사 텍스트 라벨

### 재생목록 화면
- `scl_playlist`: 재생목록 스크롤 영역
- `list_playlist`: 재생목록 리스트 위젯
- `btn_download`: 다운로드 버튼

### 컨트롤 영역
- `btn_play`, `btn_pause`, `btn_stop`: 재생 컨트롤
- `btn_previous`, `btn_next`: 이전/다음 곡
- `sld_music`: 음악 진행 슬라이더
- `sld_volume`: 볼륨 슬라이더
- `btn_volume_H`, `btn_volume_L`, `btn_volume_mute`: 볼륨 버튼
- `btn_suffle`, `btn_repeat`, `btn_repeat_1`: 재생 모드 버튼

## 🐛 문제 해결

### 일반적인 문제

1. **PyQt5 설치 오류**
   ```bash
   pip install PyQt5==5.15.9
   ```

2. **yt-dlp 설치 오류**
   ```bash
   pip install yt-dlp==2023.12.30
   ```

3. **FFmpeg 오류 (다운로드 시)**
   - FFmpeg 설치 필요: https://ffmpeg.org/download.html

4. **UI 파일 로드 오류**
   - `mp3.ui` 파일이 프로젝트 폴더에 있는지 확인

5. **이미지 파일 오류**
   - `imgs/` 폴더에 필요한 이미지 파일들이 있는지 확인

### 로그 확인

애플리케이션 실행 시 콘솔에서 로그를 확인할 수 있습니다.

## 🤝 기여하기

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 📞 지원

문제가 발생하거나 질문이 있으시면 이슈를 생성해주세요.

---

**MP3 플레이어**로 즐거운 음악 감상을 하세요! 🎵✨ 