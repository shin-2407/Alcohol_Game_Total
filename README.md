# 🍻 술게임 라이브러리 (Total_Game) 

**DrunkFunLib**는 술자리에서 즐길 수 있는 다양한 게임들을 손쉽게 구현할 수 있도록 도와주는 Python 라이브러리입니다!

---

## 🚀 주요 기능

1. **비용 계산**  
   - 영수증 사진과 인원 수를 입력하면, 총 비용을 계산하여 1인당 부담해야 할 금액을 정산해 줍니다.

2. **취한 정도 파악 게임**  
   - 음성 파일을 입력하면 문장 정확도를 기반으로 사용자의 취한 정도를 측정합니다.

3. **사진 벌칙 게임**  
   - 사용자가 업로드한 사진 속 손 모양을 분석하고 랜덤하게 벌칙 대상을 선택합니다.

4. **사진 기반 인물 퀴즈**  
   - 사용자 지정 사진을 입력해 인물 퀴즈를 진행할 수 있습니다.

5. **룰렛 벌칙 게임**  
   - 사용자가 입력한 벌칙 리스트로 룰렛을 돌려 랜덤하게 벌칙을 선정합니다.

---

## 사용방법
```python
from total_game import total_game

tg = total_game()

#비용 계산
tg.Receipt()

#취한 정도 파악 게임
tg.PronunciationApp()
(음성파일은 반드시 웨이브 파일로 업로드 해야합니다.)
ex) pronunciation.wav

#사진 벌칙 게임
tg.GroupPhotoAnalyzerApp()

#사진 기반 인물 퀴즈
images = [
    {"image": "path_to_image_1.jpg", "answer": "Person 1"},
    {"image": "path_to_image_2.jpg", "answer": "Person 2"}
]
tg.GuesseGameApp(images)

#룰렛 벌칙 게임
tg.RoulettGame(['벌칙1','벌칙2','벌칙3'])
```

---

## 📦 설치 방법

### Prerequisites
- Python 3.8 이상이 필요합니다

#### 🛠️ Tesseract OCR 설치 방법

이 프로젝트의 영수증 비용 계산 기능을 사용하기 위해서는 Tesseract OCR 설치가 필요합니다.

#### macOS
1. Homebrew를 사용하여 Tesseract를 설치합니다.
   - `brew install tesseract`
2. 설치 확인:
   - 터미널에서 `tesseract --version` 명령어를 실행해 Tesseract 버전이 출력되는지 확인하세요.

#### Ubuntu/Linux
1. APT 패키지 관리자를 사용하여 Tesseract를 설치합니다.
   - `sudo apt-get update`
   - `sudo apt-get install tesseract-ocr`
2. 설치 확인:
   - 터미널에서 `tesseract --version` 명령어를 실행해 Tesseract 버전이 출력되는지 확인하세요.

#### Windows
1. [Tesseract 다운로드 페이지](https://github.com/UB-Mannheim/tesseract/wiki)에서 설치 파일(.exe)을 다운로드합니다.
2. 설치 중 "Add Tesseract to PATH" 옵션을 선택하세요.
3. 설치가 완료된 후 Tesseract 경로를 확인합니다.
   - 기본 경로: `C:\Program Files\Tesseract-OCR\tesseract.exe`
  

4. 환경 변수 설정이 필요한 경우:
   - "내 PC" → "속성" → "고급 시스템 설정" → "환경 변수"로 이동합니다.
   - "Path" 변수에 Tesseract 설치 경로를 추가하세요.

---

## 🤝 기여하기

DrunkFunLib에 기여하고 싶으신가요? 저희는 항상 새로운 아이디어와 개선을 환영합니다!

1. 이 레포지토리를 포크하세요.
2. 새로운 브랜치를 생성하세요. (git checkout -b feature-새기능)
3. 변경사항을 커밋하세요. (git commit -m '새로운 기능 추가')
4. 브랜치를 푸시하세요. (git push origin feature-새기능)
5. Pull Request를 생성하세요.

---

## 📝 라이선스
이 프로젝트는 [MIT 라이선스](LICENSE)에 따라 배포됩니다.

---

즐거운 술자리를 위해 DrunkFunLib와 함께하세요! 🎉

