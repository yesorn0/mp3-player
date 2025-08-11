# 🎵 Python 기반 YouTube MP3 다운로드 & 가사 지원 MP3 플레이어

📌 **YouTube에서 음원을 MP3로 다운로드하고, 음원 재생과 재생목록 관리까지 지원하는 PyQt5 기반 MP3 플레이어 프로젝트**

---

## 📸 예시 화면

<img width="960" alt="player" src="https://github.com/user-attachments/assets/b74f28d4-22af-48fe-adbf-c6ef5f9f19c6" />
<img width="960" alt="lyrics" src="https://github.com/user-attachments/assets/13cef43c-2376-43f3-8cd1-8ee8e32d30b8" />
<img width="960" alt="search" src="https://github.com/user-attachments/assets/d1b8092b-81c7-4ede-abf9-949378521b8c" />

---

## 🚀 소개

이 프로그램은 다음 기능을 제공합니다.

- **YouTube 음원 다운로드** → `yt_dlp`를 사용해 최고 음질로 추출 후 MP3 변환
- **썸네일 자동 저장** → 곡별 이미지 파일(`img/` 폴더)에 저장
- **가사 자동 검색** → 네이버/구글 크롤링 기반 자동 가사 수집 *업데이트 필요
- **MP3 재생** → PyQt5 `QMediaPlayer` 기반으로 재생/일시정지/정지 지원
- **재생목록 관리** → 중복 방지, 시작 시 자동 로드
- **가사 편집/저장** → 수동 편집 가능, JSON/텍스트 파일 저장

---

## 📂 폴더 구조

```bash
project/
├─ main.py # 실행 파일
├─ mp3.ui # PyQt5 UI 파일
├─.gitignore
├─ requirements.txt
├─ download/ # MP3 저장 폴더 (자동 생성)
├─ img/ # 썸네일 저장 폴더 (자동 생성)
├─ lyrics/ # 가사 텍스트 저장 폴더 (자동 생성)
├─ playlist.json # 재생목록 데이터
└─ lyrics.json # 가사 데이터
```

---

## ⚙️ 설치 방법

### 1) Python 환경 준비

```bash
# (선택) 가상환경 생성
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
```


### 2) 라이브러리 설치

```bash
pip install -r requirements.txt
```

일부 환경에서는 PyQt5-sip, PyQt5-Qt5가 필요할 수 있습니다.


### 3) FFmpeg 설치

yt_dlp가 MP3 변환 시 필요합니다.

### Windows: FFmpeg 공식 사이트에서 다운로드 후 bin 폴더를 PATH에 추가

### macOS:

```bash
brew install ffmpeg
```

### Ubuntu/Debian:

```bash
sudo apt-get install ffmpeg
```

### ▶ 실행 방법

```bash
python main.py
```

---

## 🎯 주요 기능
✅ YouTube MP3 다운로드 (썸네일 포함)
✅ 가사 자동 검색 및 편집
✅ 재생목록 자동 로드/저장
✅ 썸네일 표시
✅ 재생, 일시정지, 정지, 이전/다음 곡, 볼륨 조절

---

## ⚠️ 주의사항
yt_dlp 사용은 YouTube 이용약관을 준수해야 합니다.

가사 크롤링 기능은 일부 사이트 구조 변경 시 동작하지 않을 수 있습니다.

가사/음원은 저작권법을 준수하여 개인 용도로만 사용하세요.

---

## 📄 라이선스
MIT License

---

## 📧 연락처
안진홍 - ajh9703@gmail.com


