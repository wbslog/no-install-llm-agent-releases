<div align="center">

# nila (니라)

### No Install LLM Agent — 설치 없이 실행하는 로컬 AI 에이전트

**One file. Any LLM. Your whole PC.**
**파일 하나로, 원하는 LLM으로, 내 PC의 실제 작업까지.**

`v1.6.1` · 2026-10-06 · Windows x64 / ARM64 · macOS Apple Silicon / Intel

</div>

---

## ⬇ Download · 다운로드

| Platform · 플랫폼 | File · 파일 |
|---|---|
| **Windows x64** | [nila-windows-x64.exe](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.6.1/nila-windows-x64.exe) |
| Windows ARM64 | [nila-windows-arm64.exe](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.6.1/nila-windows-arm64.exe) |
| **macOS Apple Silicon (M1–M4)** | [nila-1.6.1-macos-arm64.zip](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.6.1/nila-1.6.1-macos-arm64.zip) |
| macOS Intel | [nila-1.6.1-macos-x64.zip](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.6.1/nila-1.6.1-macos-x64.zip) |

- **Windows** — Save the exe anywhere and double-click. If SmartScreen appears: *More info → Run anyway*.
  받은 exe를 원하는 폴더에 두고 실행하세요. SmartScreen 경고 시 **추가 정보 → 실행**.
- **macOS** — Unzip and open `nila.app`. If Gatekeeper blocks it: `xattr -cr nila.app` (or right-click → Open).
  압축을 풀고 `nila.app` 실행. 차단되면 터미널에서 `xattr -cr nila.app` 또는 우클릭 → 열기.
- **Auto update · 자동 업데이트** — Once installed, nila checks this repository on every start and updates itself.
  한 번 실행한 뒤에는 시작할 때마다 이 저장소를 확인해 스스로 최신 버전으로 업데이트합니다.

---

## English

**nila** is a portable AI agent that runs from a single executable — no installer, no runtime, no admin rights.
Connect the model you prefer and nila works directly on your computer: it reads and edits files, organizes folders,
analyzes documents and images, browses the web, and runs commands — with you in control of every change.

### Why nila
- **Truly portable** — one ~10 MB file. Settings, chats, memory and backups live in a `nila_data` folder next to it. Copy the folder to a USB stick and your agent comes with you.
- **Bring your own model** — Claude, ChatGPT, Gemini, or your own server (Ollama, LM Studio, vLLM, any OpenAI-compatible API). Register several connections and switch with `/model` in the middle of a conversation — the context carries over.
- **Use your subscription, not an API key** — *Account login* opens the official Claude / ChatGPT / Google sign-in page. The vendor's official CLI receives the token; nila never sees your password.
- **Real work on your PC** — list, read, write, patch, move, copy and delete files anywhere (relative to a work folder or by absolute path), run PowerShell / shell commands, open files in their default app.
- **Built-in document & image tools** — read Excel / Word / PowerPoint, view and analyze images through your model, crop / resize / rotate / overlay images — without Python, Office or Photoshop.
- **Web & news** — fetch any page like a real browser, extract exactly what you need with CSS selectors or table extraction, and search five major Korean business outlets through Google News RSS for any time window.
- **Safe by design** — *Manual* approval mode shows a diff before any file change or command; *Auto* mode runs freely. Originals are backed up before edits and deletions; system folders are protected.
- **Never loses the thread** — work keeps running through page reloads and chat switches, messages queue up while the agent is busy, long conversations are summarized automatically near the context limit, and long-term memory persists across sessions.

### Highlights
| | |
|---|---|
| 🧠 Thinking level | Normal / High / Ultra — mapped to each provider's reasoning effort |
| 📊 Context gauge | Live context usage with automatic compaction (`/compact`) |
| ⌨️ Slash commands | `/help` `/clear` `/model` `/folder` `/mode` `/memory` `/history` `/compact` `/think` `/export` `/stop` `/settings` `/update` `/version` |
| 🧾 Answer footer | Tokens, elapsed time, finish time and one-click copy on every answer |
| 🌗 Themes | Light / Dark, custom window title, font size |
| 🔄 Updates | Signed-hash verified self-update from this repository |

### Privacy & security
- Local server bound to `127.0.0.1` only, with a fresh random token on every launch.
- API keys stay in `nila_data/config.json` on your machine. Account-login tokens are kept by the official CLIs.
- Web-chat scraping is deliberately **not** used: it violates the services' terms and puts accounts at risk.

### Requirements
Windows 10/11 or macOS 11+, and Microsoft Edge or Google Chrome (used as the app window; falls back to the default browser).
Account login for Gemini downloads a portable Node.js automatically if none is installed.

---

## 한국어

**nila(니라)** 는 실행 파일 하나로 동작하는 **무설치 AI 에이전트**입니다. 설치 프로그램도, 런타임도, 관리자 권한도 필요 없습니다.
원하는 LLM을 연결하면 nila가 **내 PC에서 직접** 파일을 읽고 고치고, 폴더를 정리하고, 문서와 이미지를 분석하고, 웹을 조사하고,
명령을 실행합니다. 모든 변경은 사용자가 통제합니다.

### 이런 점이 다릅니다
- **진짜 포터블** — 약 10MB 파일 하나. 설정·대화·기억·백업은 옆의 `nila_data` 폴더에 저장되어, 폴더째 USB로 옮기면 그대로 이어서 씁니다.
- **원하는 LLM 연결** — Claude, ChatGPT, Gemini, 사내·자체 LLM(Ollama, LM Studio, vLLM 등 OpenAI 호환). 여러 연결을 등록해 두고 대화 도중 `/model`로 바꿔도 **맥락이 그대로 이어집니다**.
- **API 키 없이 구독 계정으로** — [계정 로그인]을 누르면 Claude·ChatGPT·Google **공식 로그인 페이지**가 열립니다. 인증 토큰은 각사 공식 CLI가 받아 보관하며, **nila는 비밀번호를 보지도 저장하지도 않습니다.**
- **PC에서 실제로 일하는 에이전트** — 작업 폴더 기준 또는 절대 경로로 PC 어디든 파일 조회·작성·부분 수정·이동·복사·삭제, PowerShell/셸 명령 실행, 기본 프로그램으로 열기.
- **문서·이미지 도구 내장** — 엑셀·워드·파워포인트 읽기, 이미지 분석(연결한 모델로 전송), 자르기·크기·회전·투명도·여러 장 오버레이 합성까지 **Python·Office·포토샵 없이** 처리합니다.
- **웹·뉴스 조사** — 실제 브라우저처럼 페이지를 가져와 본문·링크·CSS 선택자로 특정 태그·표만 추출. 매일경제·머니투데이·이데일리·파이낸셜뉴스·한국경제를 Google News RSS로 언론사별 검색해 "최근 N일" 기사를 요약·보고합니다.
- **안전한 기본값** — **수동** 모드는 파일 변경·명령 실행 전 변경 내용(diff)을 보여주고 승인을 받습니다. **자동** 모드는 즉시 실행합니다. 수정·삭제 전 원본은 자동 백업되고, 시스템 폴더는 보호됩니다.
- **맥락을 잃지 않음** — 새로고침·채팅 이동에도 작업은 계속되고, 작업 중 보낸 메시지는 대기열로 순서대로 처리됩니다. 컨텍스트 한도에 가까워지면 이전 내용을 자동 요약하고, 장기 기억은 세션을 넘어 유지됩니다.

### 주요 기능
| | |
|---|---|
| 🧠 사고력 수준 | 보통 / 높음 / 울트라 — 각 LLM의 추론 강도로 자동 변환 |
| 📊 컨텍스트 게이지 | 실시간 사용량 표시, 한도 근접 시 자동 요약(`/compact`) |
| ⌨️ 명령어 | `/help` `/clear` `/model` `/folder` `/mode` `/memory` `/history` `/compact` `/think` `/export` `/stop` `/settings` `/update` `/version` |
| 🧾 답변 정보 | 답변마다 소모 토큰·소요 시간·완료 시간·복사 버튼 |
| 🌗 테마 | NORMAL / DARK, 프로그램 타이틀·글자 크기 설정 |
| 🔄 자동 업데이트 | 이 저장소에서 SHA-256 검증 후 스스로 업데이트 |

### 개인정보 · 보안
- 로컬 서버는 `127.0.0.1`에만 열리며, 실행할 때마다 새 보안 토큰을 발급합니다.
- API 키는 내 PC의 `nila_data/config.json`에만 저장됩니다. 계정 로그인 토큰은 각사 공식 CLI가 보관합니다.
- 웹 채팅 화면을 긁어오는 방식은 서비스 약관 위반·계정 정지 위험 때문에 **사용하지 않습니다**.

### 실행 환경
Windows 10/11 또는 macOS 11 이상, Microsoft Edge 또는 Google Chrome(앱 창으로 사용 — 없으면 기본 브라우저).
Gemini 계정 로그인은 Node.js가 없으면 휴대용 Node.js를 자동으로 받아 사용합니다.

---

## Version history · 버전 기록

### v1.6.1 (2026-10-06)

- 자동 업데이트로 다시 시작된 nila가 열려 있는 창을 추적하지 못해, 창을 오래 두면 여전히 스스로 종료되어 재연결이 안 되던 문제 수정 — 업데이트 전 창의 프로세스를 넘겨받아 창이 실제로 닫힐 때만 종료
- 사용량(토큰·크레딧) 한도로 작업이 멈추면 안내와 함께 [이어서 진행] / [새로 시작] 버튼 표시 — 한도가 초기화되거나 충전한 뒤 [이어서 진행]을 누르면 같은 대화에서 멈춘 지점부터 계속, [새로 시작]은 새 대화에 마지막 요청을 넣어 줌 (HTTP 402/429, 크레딧 부족, CLI 사용 한도 등 인식)
- 컨텍스트 한도 초과로 작업이 멈추던 문제 자동 해결 강화: 서버가 알려준 숫자로 답변 길이 예약을 정확히 줄여 재시도, 한 요청 안에서 도구를 많이 쓴 긴 작업도 중간 단계까지 요약, 모든 도구 결과·이전 파일 내용 축소, 프로젝트 지침·기억 생략 순으로 단계적 재시도
- 보내기 전에 크기를 미리 계산해 넘치기 전에 요약, 요약 요청 자체도 컨텍스트에 맞게 줄임
- 모델 서버가 알려준 실제 컨텍스트 크기를 연결 설정에 자동 저장 (컨텍스트 크기를 비워 둔 경우)

### v1.6.0 (2026-10-06)

- 프로젝트 지침 파일(Claude Code의 CLAUDE.md와 같은 방식): 작업 폴더의 NILA.md(프로젝트 지침)·NILA.local.md(개인)·nila_data/NILA.md(모든 폴더 공통)를 대화마다 자동으로 읽어 항상 참고 — 파일 안에서 '@.nila/guide.md' 한 줄로 다른 파일 포함
- 검증 명령(.nila/harness.json): 파일을 바꾼 작업 끝에 verify 명령(테스트·검사)을 실행해 확인하고 실패하면 수정, /harness 로 바로 실행
- 경로별 규칙(.nila/rules/*.md, 'paths: web/**'): 해당 파일을 다룰 때만 규칙을 넣음
- 작업 기록(.nila/worklog.md): 작업이 끝날 때마다 요청·상태·변경 파일·결과를 자동 추가(설정에서 켜기, 기본 꺼짐), 최신 10개를 다음 대화에 자동 반영
- /init: 폴더를 분석해 NILA.md·harness.json 초안 작성, /memory: 로드된 지침 파일과 토큰 수 표시
- 모델 컨텍스트 크기의 약 1/8 안에서만 넣어 작은 로컬 모델(32K)에서도 안전, Claude Code·Codex CLI 연결에도 적용

### v1.5.4 (2026-10-06)

- 창을 오래 사용하지 않으면(Windows·브라우저가 창을 일시 정지) nila가 창이 닫힌 것으로 판단해 스스로 종료되던 문제 수정 — nila 창이 열려 있는 동안에는 종료하지 않음
- [지금 다시 연결]을 누르면 '확인 중…'으로 진행 상태를 표시하고, 연결에 실패하면 원인·확인 방법·조치를 알림창으로 안내 (nila 미실행 / 응답 없음 / 재시작되어 접속 정보 불일치 / 오류 응답 구분, 로그 파일 위치, 진단 정보 복사)
- 재연결이 계속 실패하면 상단 안내에 'nila 프로그램이 실행 중이 아닌 것 같습니다' 표시

### v1.5.3 (2026-10-02)

- 연결이 끊기면(PC 절전·오래 사용 안 함·네트워크 불안정) 'Failed to fetch' 오류 팝업 대신 화면 최상단에 연결 끊김 안내를 계속 표시 — X로 닫거나 다시 연결되면 자동으로 닫힘
- 끊긴 동안 자동으로 주기적 재연결(3초부터 점점 늘려 최대 30초 간격), [지금 다시 연결] 버튼, 채팅창에 입력하거나 전송하면 바로 재연결 시도 (전송 실패 시 입력 내용 유지)
- 다시 연결되면 실행 중인 작업 화면·채팅 목록을 자동 복원
- PC 절전에서 깨어났을 때 nila가 창이 닫힌 것으로 오인해 스스로 종료되던 문제 수정 (창 응답 대기 시간 2.5분 → 5분, 절전 복귀 감지)
- 인터넷 연결이 끊기면 LLM 응답을 받을 수 없다는 안내 표시

### v1.5.2 (2026-10-01)

- 프로그램 창 제목에 현재 버전 표시 (예: nila 1.5.2)

### v1.5.1 (2026-10-01)

- LLM 연결 방식을 서비스별 지원 여부에 맞게 자동 제한: Gemini는 API 키만 선택 가능 (Google이 2026-06-18부터 개인 계정의 Gemini CLI 사용을 중단), 계정 로그인 버튼은 비활성화하고 이유 표시
- 기존 Gemini 계정 로그인 연결은 자동으로 API 키 방식으로 전환 — API 키를 입력하면 바로 사용
- Claude Code·ChatGPT 계정 로그인 선택 시 요금 안내 표시 (Claude: 도구에서 쓰면 별도 월 크레딧 차감, ChatGPT: 요금제 사용량·5시간 단위 한도)
- 채팅창 위 '이전 대화' 목록을 한 줄로 줄여 대화 영역을 더 넓게 표시 (높이 약 1/3)

### v1.5.0 (2026-10-01)

- 작업 폴더 이어서 작업: 새 대화에서 작업 폴더를 지정하면 그 폴더에서 마지막으로 작업한 대화가 자동으로 열려 대화 전체를 그대로 이어서 작업 (PC 재시작 후에도 동일, 설정 > 에이전트에서 끌 수 있음)
- 채팅창 위에 이 폴더의 이전 대화 목록(제목·시간·메시지 수·마지막 요청) 표시 — 누르면 열기, [더 보기]로 전체 목록, 접기 가능 (표시 수 설정, 기본 3개)
- 프로그램 종료·PC 재시작으로 끝나지 않은 작업은 '중단됨'으로 표시하고 [이어서 진행]으로 중단된 지점부터 계속
- 폴더별 마지막 작업 상태(최근 요청·변경한 파일·마지막 답변)를 매 작업마다 자동 기록해, 그 폴더에서 새 대화를 시작해도 nila가 이전 작업 맥락을 알고 시작 (LLM에 알려줄 이전 대화 수 설정, 기본 10개)
- 채팅 목록을 캐시해 대화가 많아도 목록·검색이 빠르게 열림

### v1.4.2 (2026-10-01)

- Gemini CLI가 개인 Google 계정 사용 중단(IneligibleTierError)으로 실패하면, 재설치·재로그인 안내 대신 [API 키] 방식 전환(aistudio.google.com/apikey) 또는 Workspace 계정 로그인을 먼저 안내
- Google Cloud 프로젝트 지정이 필요한 계정(GOOGLE_CLOUD_PROJECT)도 원인과 해결 방법을 안내
- CLI 오류는 설명을 먼저 보여주고 긴 CLI 원문은 뒤에 표시

### v1.4.1 (2026-09-30)

- Gemini CLI 자동 설치가 성공했는데도 '설치 후 실행 파일을 찾지 못했습니다' 오류로 끝나던 문제 수정 (설치 완료 판정 오류)
- CLI가 사용 가능하면 이전 설치 실패 메시지를 더 이상 표시하지 않음

### v1.4.0 (2026-09-30)

- 로컬 뉴스 인덱스(RAG): 설정 > 뉴스에서 관심 주제·주요 뉴스를 주기적으로 수집해 PC에 저장하고, 질문할 때 관련 기사를 자동으로 찾아 함께 전달 — 로컬 모델도 최신 소식으로 답변 (search_news 결과도 자동 저장, search_news_index 도구, 검색 테스트, /news)
- 되돌리기: 질문 말풍선의 [되돌리기] 또는 /rewind 로 그 질문 직전으로 대화와 nila가 바꾼 파일(쓰기·수정·삭제·이동·복사·이미지 저장)을 복원, 질문은 입력창에 다시 채움 ('대화만 되돌리기' 선택 가능)
- 하위 에이전트(run_subagents): 서로 독립적인 조사 작업을 읽기 전용 하위 에이전트로 나눠 동시에 실행하고 보고서만 받아 종합 — 진행 상황을 작업 카드에 표시, 동시 실행 수는 설정 > 에이전트
- 자체 LLM 사고 모드 제어: Qwen3 등에서 사고력 '보통' = 사고 끔(빠른 답변), '높음·울트라' = 사고 켬 (chat_template_kwargs 또는 /think·/no_think 방식 선택)
- 자체 LLM이 답변 앞에 붙이는 <think>…</think>를 스트리밍 중에도 사고 과정으로 분리해 표시

### v1.3.3 (2026-09-30)

- 업데이트 설치가 실행 중인 작업을 기다리는 동안 '진행 중인 작업 N개가 끝나면 설치합니다'로 안내하고 [작업 중지하고 지금 설치] 버튼 제공 (계속 '설치 중'으로 보이던 문제)
- 업데이트 적용이 두 번 실행되지 않도록 보호

### v1.3.2 (2026-09-30)

- 답변 작성 중 소요 시간·토큰 수 실시간 표시(1초마다 갱신, 파일 내용 등 도구 입력 생성량 포함, '작성 중 (약 N자)' 진행 표시)
- 작성 중 상태 줄에 '파일 쓰기 작성 중… (약 N자)'처럼 도구 입력 생성량 표시 — 큰 파일을 만들 때 멈춘 것처럼 보이던 문제 개선

### v1.3.1 (2026-09-30)

- 설정 > 업데이트: 업데이트 설치 시 단계별 진행 화면(① 다운로드 % → ② 설치 → ③ 다시 시작) 표시, 완료되면 자동 새로고침
- 페이지를 연 지 40초 뒤 설치를 누르면 진행 표시·자동 새로고침이 멈추던 문제 수정
- '버전 확인' 표기를 '업데이트'로 통일
- 좌측 메뉴 상단의 로고·타이틀·접기(<) 줄 제거 (메뉴 보기/감추기는 상단 토글 아이콘·Ctrl+B)
- 사용자 지정 지침에 일반적인 기본 지침을 기본값으로 제공(비어 있을 때 1회 채움) + '기본 지침으로 되돌리기' 버튼
- 설정의 ? 도움말 말풍선이 창 가장자리에서 잘리지 않도록 위치 자동 조정
- 계정 로그인: CLI 설치가 끝나기 전에 로그인 버튼이 활성화되어 Gemini CLI가 파일 누락 오류로 실행되던 문제 수정(설치 완료 확인 후에만 사용 가능 표시)
- 대기열 메시지 취소: 취소선으로 표시하고 실행 중지, 이후 삭제 아이콘으로 실제 삭제

### v1.3.0 (2026-09-30)

- 계정 로그인: Claude·ChatGPT·Google 공식 로그인 페이지로 로그인해 API 키 없이 구독 계정으로 사용 (공식 CLI 자동 설치: Claude Code·Codex CLI·Gemini CLI, 휴대용 Node.js 포함) — 비밀번호는 nila가 보거나 저장하지 않음
- 대화 도중 LLM 연결을 바꿔도(API↔계정 로그인 포함) 요약+최근 대화를 넘겨 맥락을 이어서 작업
- 명령어 입력 후 Enter로 바로 실행되지 않던 문제 수정, /model 입력 시 등록된 연결 목록에서 선택
- 설정 메뉴 순서 변경(일반·LLM 설정·에이전트·업데이트·버전 기록·도움말·프로그램 설명), 에이전트 설정 항목별 ? 도움말
- 상단에 프로그램 위치 표시 + 클릭 시 폴더 열기, 알림 메시지를 화면 최상단 가운데에 표시
- 릴리즈 저장소 README를 영문·한글 소개로 개편, 프로그램 한글 이름 '니라' 표기

### v1.2.1 (2026-09-30)

- 승인 모드(수동/자동)·사고력(보통/높음/울트라)을 위로 열리는 드롭다운으로 변경(항목별 설명), 컨텍스트 게이지를 그 옆으로 이동
- 질문에 날짜·시간과 복사 버튼, 답변 끝에 소모 토큰·소요 시간·완료 시간과 복사 버튼 표시
- 소형 컨텍스트 모델(예: 32K 로컬 LLM) 대응: 도구 결과 크기를 컨텍스트 한도에 맞춰 자동 조절, 한도 초과 시 요약→결과 축소→출력 예약 축소 순으로 자동 재시도
- 자체 LLM 설정에 '컨텍스트 크기' 항목 추가, '맥락' 표기를 '컨텍스트'로 통일
- 설정 > 업데이트에서 업데이트 설치 시 실행 중 작업 종료 후 자동 재시작, 재시작 후 '업데이트 완료' 안내

### v1.2.0 (2026-09-30)

- 작업이 새로고침(F5)·채팅 이동·창 닫힘에도 서버에서 계속 진행되고, 다시 열면 이어서 표시
- 실행 중에도 메시지 전송 가능 — 대기열에 쌓여 순서대로 처리(취소 가능)
- 슬래시 명령어: /help /clear /model /folder /mode /memory /history /export /stop /settings /update /version
- 입력창 ↑/↓ 로 이전 입력 불러오기, Ctrl+B 좌측 메뉴 토글, 창 폭 100% 사용·좁은 창에서 메뉴 자동 숨김
- LLM 연결 목록: 여러 연결을 등록하고 선택/전환(/model), 연결 방식 'API 키' 또는 '로그인(공식 CLI: Claude Code·Gemini CLI·Codex CLI)' 선택, 로그인 방식 주의사항 안내
- 기억: 마지막 대화 자동 복원, save_memory로 저장한 기억을 매 대화에 반영(/memory), search_history로 이전 대화 검색
- 웹 페이지 분석(fetch_url: 브라우저처럼 접속·본문/링크 추출)과 경제지 5곳 뉴스 검색·요약(search_news, Google News RSS, 최근 N일)
- 이미지 편집/합성 내장(image_edit·image_compose: 자르기·크기·회전·투명도·오버레이) — 외부 프로그램 불필요
- 임시 보조 파일 자동 정리 지침, 토큰 사용량 단위·합계 표시, 버전 확인 시 진행 표시
- 사고력 수준(보통/높음/울트라) 선택, 컨텍스트 사용량 게이지, 한도 근접 시 자동 요약(컨텍스트 정리)·/compact
- 크롤링: CSS 선택자로 특정 태그 추출(mode=select, 텍스트/HTML/속성), 표 추출(mode=tables), Google News 링크 원문 해석
- 설정창 확대(창 크기에 맞춰 축소), 채팅 기록 전체 삭제 버튼 위치·외곽선, 작성 중 스피너 회전 수정

### v1.1.0 (2026-09-30)

- 자동 업데이트: 실행 시 새 릴리즈를 확인해 자동으로 받아 교체 후 같은 창에서 다시 실행 (없으면 그대로 실행)
- 설정 > 업데이트: 현재/최신 버전, 업데이트 확인·설치 버튼, 시작 시 자동 업데이트 설정
- 이미지 분석 도구(view_image): PC의 이미지 파일을 연결된 LLM으로 분석, 큰 이미지 자동 축소, BMP/WebP 지원
- 엑셀(.xlsx)·워드(.docx)·파워포인트(.pptx) 내장 읽기 — Python·Office 설치 불필요
- 응답 출력 중 다른 채팅으로 이동했다가 돌아와도 이어서 출력
- nila 전용 아이콘으로 교체, 프로그램 설명에서 시스템 정보 제거

### v1.0.0 (2026-09-30)

- 최초 릴리스 — nila(No Install LLM Agent), 무설치(포터블) 단일 실행 파일, Windows(x64/ARM64) · macOS(Apple Silicon/Intel) 지원
- Claude 스타일 채팅 UI, NORMAL/DARK 테마, 프로그램 타이틀 지정
- LLM 연결: 자체 LLM(OpenAI 호환), Claude(API 키 / Claude Code CLI), Gemini, ChatGPT — 설정·연결 테스트·모델 목록 불러오기
- 로컬 파일 에이전트 도구: 폴더 조회, 파일 읽기/쓰기/부분 수정, 검색, 삭제, 이동, 복사, 폴더 생성, OS로 열기, 셸 명령 실행
- 수동/자동 승인 모드, 변경 diff 미리보기, 수정·삭제 전 자동 백업
- 작업 폴더 선택(네이티브 대화상자) · 직접 입력 · 최근 폴더, 절대 경로 지원
- 파일/이미지 첨부(버튼·드래그·붙여넣기), UTF-8/UTF-16/EUC-KR 자동 인식
- 채팅 기록 저장(1~30일 자동 정리), 검색·이름 변경·삭제·전체 삭제·Markdown 내보내기
- 토큰 사용량 집계/초기화, 실행 중지, 도움말·버전 기록·프로그램 설명


---

<div align="center">

nila (니라) — No Install LLM Agent · This repository hosts release builds only · 빌드 배포 전용 저장소

</div>
