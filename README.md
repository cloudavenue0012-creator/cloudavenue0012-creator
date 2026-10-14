# Ethan · Finance × AI (AX)

외식 프랜차이즈 **재무 8년차**이자 사내 **Finance팀 AI 관리자(챔피언)**.
재무 도메인을 떠나지 않고, 반복·정산·손익 프로세스를 **직접 AI로 재설계·자동화하고 매일 운영**합니다 — 기획만 하는 사람과 코드만 짜는 사람 사이, 현업 문제를 스스로 빌드하고 성과까지 책임지는 지점에서 일합니다.

> **설계 원칙 —** AI 산출물도 무검증으로 신뢰하지 않습니다. 신뢰는 무결함이 아니라 *"틀려도 걸러진다"* 는 **검증 게이트**에서 나옵니다.

### 🏭 지금 운영 중인 것 (2026-10 기준)
POC가 아니라 **매일 돌아가는 업무 시스템**입니다. 회사 데이터·코드는 공개하지 않고, 같은 설계를 합성 데이터로 재구현한 것이 아래 대표 프로젝트입니다.

- **무인 배치 약 60개 상시 운영** — 매일 아침 데이터 적재 → 대시보드 갱신 → 보고 메일·메신저까지 사람 손 없이. 실패는 감독자가 감지·복구하고, exit 코드가 아니라 **산출물로 성공을 판정**합니다.
- **역할을 나눈 AI 에이전트 세션 10개** — 손익·매출·정산·자금·회의 등 도메인별로 나눠 동시에 운영. 커밋·공용 파일은 한 세션만 쓰는 **단일 커미터 규약**, 상황판으로 진행·막힘을 한 화면에.
- **재사용 업무 절차(스킬) 130여 개** — 실수가 나면 같은 날 절차·게이트로 고정해 재발을 막습니다.

| 영역 | 하는 일 |
|---|---|
| 손익(P&L) | 월 손익 마감·예상손익 대시보드, 증감을 물량·가격·원가·환율로 분해, 일회성·조정 이력 추적 |
| 매출 | 프로모션 규칙으로 시스템 매출을 **독립 재계산**해 원장과 3-way 대사, 동일 매장 성장률(SSSG) 일일 보고 |
| 정산·자금 | 배달앱 정산 출금 RPA(전 매장 무인), 자금일보 초안 자동 작성과 확정본 대비 채점 |
| 원가·투자 | 원가 DB 대시보드(품목 원가·재고·마진 예측), 신규 매장 투자회수(Payback·NPV) 검증, 유통마진 추정 엔진들을 매달 실적으로 채점 |
| 문서 수집 | 매장 고지서 제출 웹폼 → VLM 판독 → 금액 대사 → 미제출 독촉까지 |
| 회의·보고 | 회의 녹취 → 회의록 → 액션 추적 → **매장 단위로 성과 판정**, 임원 질문 예측·가상 보고 리허설 |
| 시장 | 유튜브·뉴스 소비자 반응을 주제별로 수집하고 **로컬 LLM**으로 어조 분류 |

### 🔧 Stack
`Python` · `SQL (PostgreSQL)` · `pandas` · `Playwright (RPA)` · `Cloudflare Pages · Workers · D1` · `Streamlit` · `Excel 자동화 (win32com/openpyxl)` · `Git / GitHub Actions`
`Claude Code` 멀티 세션 오케스트레이션 · `MCP` · 로컬 LLM(`Ollama`, VLM) · 검증 게이트 설계 · 이상탐지 · 데이터 파이프라인 · 대시보드 · 무인 배치 감독(self-healing)

### 📌 대표 프로젝트 — 전량 합성 데이터, 회사 데이터 없음

**[Operating-Income Bridge](https://github.com/cloudavenue0012-creator/operating-income-bridge)**
영업이익 증감을 **물량·믹스·가격·원가·환율·판관비로 정확 분해**하는 FP&A 브리지. `OP0 + 6요인 = OP1` 검증항등식(잔차 0) + 심은 드라이버 **복원율 1.0** eval + 워터폴. 경영관리의 첫 질문 "왜 이익이 움직였나"에 답하는 도구.

**[Settlement Reconciliation & Verification Engine](https://github.com/cloudavenue0012-creator/settlement-reconciliation-engine)**
다채널 매출 정산을 규칙엔진으로 **독립 재계산 → 대조**하는 검증 게이트. 이상탐지 **F1 0.956 · recall 100%**, eval·튜닝곡선·**CI 게이트**·Streamlit. 리깅됐던 벤치마크를 스스로 발견·수정하고, 그 판별 로직은 **한 줄 실행으로 재현되는 스크립트**로 남겼습니다.

**[Verification-Gated Agents](https://github.com/cloudavenue0012-creator/verification-gated-agents)**
검증 게이트를 쌓으면 신뢰도가 **0.55 → 0.97+**로 오르는 곡선을 측정 — 단 **정밀한 게이트만 개선되고 노이즈 게이트는 최적점 후 하락**(과잉 게이팅 역효과). 공유상태 단일커밋터 불변식.

**[Self-Healing Automation](https://github.com/cloudavenue0012-creator/self-healing-automation)**
무인 자동화를 스스로 고치는 감독자 — 실패 감지 → **경계 안 복구행동 선택** → **exit 코드가 아닌 실제 결과 검증** → 못 고치면 사람에게 에스컬레이션. 검증을 끄면 **7%가 "복구됨"으로 보고되지만 실제론 고장**(exit-0 거짓말). RPA는 껍데기, 감독자가 본체.

**[Utility-Bill Extraction + Reconciliation Eval](https://github.com/cloudavenue0012-creator/utility-bill-extraction-eval)**
고지서 문서추출 → 대사의 **2층 eval**. *"추출 품질이 대사 F1의 천장"* 을 sweep으로 증명하고, denoise 가설을 **McNemar로 검정 → 기각**. 현실이 반박한 기록.

---
<sub>결과를 주장이 아니라 <b>측정된 수치</b>로 보여줍니다 — 다섯 repo 모두 eval·CI로 검증되고, 같은 설계가 실무에서 매일 운영됩니다.</sub>
