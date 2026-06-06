# Lupic 실습

🌐 [English](README.md) | **한국어**

Kamibot(카미봇) 교육용 로봇을 파이썬과 LLM(인공지능)으로 제어하는 실습 자료입니다.
처음 접하는 분도 따라 할 수 있도록 **설치 → 실습** 순서로 정리했습니다.

순서대로 진행하세요.

1. [USB 동글 드라이버 설치](#1단계-usb-동글-드라이버-설치)
2. [JupyterLab Desktop 설치](#2단계-jupyterlab-desktop-설치)
3. [실습 진행 (01 ~ 05)](#3단계-실습-진행-01--05)

---

## 1단계. USB 동글 드라이버 설치

Kamibot은 USB 동글(무선 통신 장치)로 PC와 연결됩니다.
**가장 먼저 드라이버를 설치해야** PC가 동글을 인식할 수 있습니다.

### 설치 방법

1. 이 저장소에 포함된 설치 파일을 실행합니다.

   ```
   CDM21228_Setup.exe
   ```

   > 파일 위치: 이 프로젝트 폴더 안에 있습니다.
   > (예: `C:\wk-app\lupic-github\lupic\CDM21228_Setup.exe`)

2. 안내 창이 뜨면 **Extract → Next → 약관 동의 → Finish** 순서로 진행합니다.
3. 설치가 끝나면 USB 동글을 PC에 꽂습니다.

> 💡 드라이버를 설치하지 않으면 실습 01에서 동글(포트)을 찾지 못합니다.
> 반드시 이 단계를 먼저 끝내 주세요.

---

## 2단계. JupyterLab Desktop 설치

실습은 **주피터 노트북(`.ipynb`)** 파일로 진행합니다.
이 노트북을 실행하려면 **JupyterLab Desktop**을 설치합니다.

### 설치 방법

1. 아래 다운로드 페이지로 이동합니다.

   👉 https://github.com/jupyterlab/jupyterlab-desktop/releases

2. 가장 위에 있는 최신 버전(Latest)에서 본인 운영체제에 맞는 설치 파일을 내려받습니다.

   - **Windows**: `JupyterLab-Setup-Windows-x64.exe`
   - **macOS**: `JupyterLab-Setup-macOS-...dmg`
   - **Linux**: `.deb` 또는 `.AppImage`

3. 내려받은 파일을 실행하여 안내에 따라 설치합니다.
4. 설치 후 **JupyterLab Desktop**을 실행합니다.

### 실습 파일 열기

1. JupyterLab Desktop 화면에서 이 프로젝트 폴더(`lupic`)를 엽니다.
2. 왼쪽 파일 목록에서 실습 노트북(`01_KAMIBOT_en.ipynb` 등)을 더블클릭하면 열립니다.

> 💡 노트북에서 코드 셀을 실행하려면 셀을 클릭한 뒤 **Shift + Enter**를 누릅니다.

---

## 3단계. 실습 진행 (01 ~ 05)

아래 순서대로 진행하세요. 노트북마다 필요한 라이브러리 설치 방법과 예제가 들어 있습니다.

| 순서 | 파일 | 내용 |
|------|------|------|
| 01 | [01_KAMIBOT_en.ipynb](01_KAMIBOT_en.ipynb) | **Kamibot 기본 제어** — 파이썬 라이브러리(`pykamilab`) 설치, 연결 포트 찾기, 로봇 움직이기 |
| 02 | [02_AGENT_en.ipynb](02_AGENT_en.ipynb) | **LangChain 에이전트 입문** — 최신 LangChain의 `create_agent`로 가장 간단한 AI 에이전트 만들기 |
| 03 | [03_LANGGRAPH_en.ipynb](03_LANGGRAPH_en.ipynb) | **LangGraph 입문** — 동일한 에이전트를 그래프(노드·엣지) 방식으로 만들어 흐름을 직접 제어하기 |
| 04 | [04_LLMtoROBOT_en.ipynb](04_LLMtoROBOT_en.ipynb) | **LLM으로 로봇 제어** — 자연어 명령을 이해해 Kamibot을 움직이는 에이전트 만들기 |
| 05 | [05_RSLtoROBOT_en.ipynb](05_RSLtoROBOT_en.ipynb) | **RSL로 로봇 제어** — LLM이 로봇 전용 언어(RSL)를 생성하고, 이를 검증·실행해 로봇을 구동하기 |

### 진행 팁

- 노트북 안의 코드 셀은 **위에서부터 순서대로** 실행하세요.
- 01번 실습은 로봇·동글이 PC에 연결되어 있어야 합니다.
- 02 ~ 05번 실습은 LLM API 키가 필요합니다(예: OpenAI 또는 Anthropic).
  노트북 안내에 따라 API 키를 준비하세요.

---

## API Key
```
import os
os.environ["OPENAI_API_KEY"] = "sk-..."

print(os.environ.get("OPENAI_API_KEY"))
```

## 준비물 요약

- Kamibot(카미봇) 로봇 본체와 USB 동글
- Windows / macOS / Linux PC
- LLM API 키 (실습 02 ~ 05에서 사용)

## 참고 링크

- JupyterLab Desktop 다운로드: https://github.com/jupyterlab/jupyterlab-desktop/releases
- pykamilab (Kamibot 파이썬 라이브러리): https://pypi.org/project/pykamilab/
- pykamirsl (RSL 라이브러리): https://pypi.org/project/pykamirsl/
