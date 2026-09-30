# nila 릴리즈 — No Install LLM Agent

설치 없이 실행하는 로컬 AI 에이전트 **nila**의 빌드 배포 저장소입니다. (빌드 결과물만 올라갑니다)

## 최신 버전: v1.2.0 (2026-09-30)

| 플랫폼 | 다운로드 |
|---|---|
| Windows x64 | [nila-windows-x64.exe](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.2.0/nila-windows-x64.exe) |
| Windows ARM64 | [nila-windows-arm64.exe](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.2.0/nila-windows-arm64.exe) |
| macOS Apple Silicon | [nila-1.2.0-macos-arm64.zip](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.2.0/nila-1.2.0-macos-arm64.zip) |
| macOS Intel | [nila-1.2.0-macos-x64.zip](https://raw.githubusercontent.com/wbslog/no-install-llm-agent-releases/main/releases/v1.2.0/nila-1.2.0-macos-x64.zip) |

- Windows: 받은 exe를 원하는 폴더에 두고 실행하세요(이름은 nila.exe 로 바꿔도 됩니다). SmartScreen 경고 시 **추가 정보 → 실행**
- macOS: 압축을 풀고 nila.app 실행. 경고가 뜨면 터미널에서 `xattr -cr nila.app`
- 설치 후에는 프로그램이 시작할 때 이 저장소의 `latest.json`을 확인해 **자동으로 업데이트**합니다 (설정 > 버전 확인).

## 버전 기록

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
- 사고력 수준(보통/높음/울트라) 선택, 맥락(컨텍스트) 사용량 게이지, 한도 근접 시 자동 요약(맥락 정리)·/compact
- 크롤링: CSS 선택자로 특정 태그 추출(mode=select, 텍스트/HTML/속성), 표 추출(mode=tables), Google News 링크 원문 해석
- 설정창 확대(창 크기에 맞춰 축소), 채팅 기록 전체 삭제 버튼 위치·외곽선, 작성 중 스피너 회전 수정

### v1.1.0 (2026-09-30)

- 자동 업데이트: 실행 시 새 릴리즈를 확인해 자동으로 받아 교체 후 같은 창에서 다시 실행 (없으면 그대로 실행)
- 설정 > 버전 확인: 현재/최신 버전, 업데이트 확인·설치 버튼, 시작 시 자동 업데이트 설정
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

