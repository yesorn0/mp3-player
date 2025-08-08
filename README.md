# 🎵 Python 기반 YouTube 음원 다운로드 및 MP3 플레이어

📌 **YouTube에서 음원을 다운로드하고, 로컬 MP3 플레이어를 통해 실제로 음원을 재생하는 파이썬 프로젝트**

---

## 📸 소개

음악 스트리밍 서비스가 없어도 원하는 노래를 간편하게 저장하고 재생해보세요!  
이 프로젝트는 Python을 이용해 YouTube에서 음원을 다운로드하고,  
GUI 또는 CLI를 통해 **MP3 음원을 직접 재생할 수 있는 기능**을 구현했습니다.  
실질적인 MP3 플레이어처럼 작동하는 인터페이스를 갖추고 있어 누구나 쉽게 사용할 수 있습니다.  
다운로드 + 재생까지 한 번에 해결! 🎧

---

## 🚀 사용 방법

### 1. 설치

먼저 필요한 라이브러리들을 설치하세요.  
(※ `pytube`, `pygame`, `pydub`, `tkinter` 등 사용)

```bash
pip install -r requirements.txt
또는 개별 설치 예:

bash
복사
편집
pip install pytube pygame pydub
🔧 ffmpeg 설치가 필요한 경우 공식 다운로드 페이지를 참고하세요.

2. 음원 다운로드
터미널 또는 GUI에서 YouTube 링크를 입력하고 다운로드 버튼을 누르면
자동으로 MP3 형식으로 변환되어 로컬 저장됩니다.

bash
복사
편집
python downloader.py
예시 입력:

arduino
복사
편집
https://www.youtube.com/watch?v=dQw4w9WgXcQ
3. MP3 재생
다운로드한 MP3 파일을 선택하여 재생합니다.
GUI 또는 콘솔에서 재생, 일시정지, 정지 등의 기능을 사용할 수 있습니다.

bash
복사
편집
python player.py
✨ 예시
입력:

YouTube 링크: https://www.youtube.com/watch?v=example123

출력:

music/ 폴더에 song_title.mp3 저장

GUI를 통한 재생 컨트롤 가능

💡 실제 재생 화면(GUI) 또는 다운로드 성공 화면 이미지를 여기에 추가해 주세요.

🛠️ 주요 기능
✅ YouTube 음원 추출 및 mp3 변환

✅ MP3 파일 저장 및 관리

✅ 음악 재생 / 일시정지 / 정지 기능 구현

✅ 간단한 GUI 또는 콘솔 기반 인터페이스

✅ 재생목록/랜덤재생(옵션 기능)

📄 라이선스
이 프로젝트는 MIT 라이선스를 따릅니다.
자세한 내용은 LICENSE 파일을 참고하세요.

📧 연락처
안진홍 - ajh9703@gmail.com

