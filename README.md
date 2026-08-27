# Ethan · Finance × AI (AX)

외식 프랜차이즈 **재무 8년차**이자 사내 **Finance팀 AI 관리자(챔피언)**.
재무 도메인을 떠나지 않고, 반복·정산·손익 프로세스를 **직접 AI로 재설계·자동화**합니다 — 기획만 하는 사람과 코드만 짜는 사람 사이, 현업 문제를 스스로 빌드하고 성과까지 책임지는 지점에서 일합니다.

> **설계 원칙 —** AI 산출물도 무검증으로 신뢰하지 않습니다. 신뢰는 무결함이 아니라 *"틀려도 걸러진다"* 는 **검증 게이트**에서 나옵니다.

### 🔧 Stack
`Python` · `SQL` · `pandas` · `Playwright (RPA)` · `Streamlit` · `Excel 자동화 (win32com/openpyxl)` · `Git / GitHub Actions`
LLM 멀티에이전트 오케스트레이션 · 검증 게이트 설계 · 이상탐지 · 데이터 파이프라인 · 대시보드

### 📌 대표 프로젝트 — 전량 합성 데이터, 회사 데이터 없음

**[Operating-Income Bridge](https://github.com/cloudavenue0012-creator/operating-income-bridge)**
영업이익 증감을 **물량·믹스·가격·원가·환율·판관비로 정확 분해**하는 FP&A 브리지. `OP0 + 6요인 = OP1` 검증항등식(잔차 0) + 심은 드라이버 **복원율 1.0** eval + 워터폴. 경영관리의 첫 질문 "왜 이익이 움직였나"에 답하는 도구.

**[Settlement Reconciliation & Verification Engine](https://github.com/cloudavenue0012-creator/settlement-reconciliation-engine)**
다채널 매출 정산을 규칙엔진으로 **독립 재계산 → 대조**하는 검증 게이트. 이상탐지 **F1 0.956 · recall 100%**, eval·튜닝곡선·**CI 게이트**·Streamlit. 리깅됐던 벤치마크를 스스로 발견·수정한 기록까지.

**[Verification-Gated Agents](https://github.com/cloudavenue0012-creator/verification-gated-agents)**
검증 게이트를 쌓으면 신뢰도가 **0.55 → 0.97+**로 오르는 곡선을 측정 — 단 **정밀한 게이트만 개선되고 노이즈 게이트는 최적점 후 하락**(과잉 게이팅 역효과). 공유상태 단일커밋터 불변식.

**[Utility-Bill Extraction + Reconciliation Eval](https://github.com/cloudavenue0012-creator/utility-bill-extraction-eval)**
고지서 문서추출 → 대사의 **2층 eval**. *"추출 품질이 대사 F1의 천장"* 을 sweep으로 증명하고, denoise 가설을 **McNemar로 검정 → 기각**. 현실이 반박한 기록.

---
<sub>결과를 주장이 아니라 <b>측정된 수치</b>로 보여줍니다 — 두 repo 모두 eval·CI로 검증됩니다.</sub>
