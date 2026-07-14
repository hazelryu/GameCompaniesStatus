# KRGameCompanyStatus

한국 게임사 실적(IR)·주요 타이틀 지표·모바일/PC 게임 순위를 추적하는 저장소.
(구 저장소명: GameCompaniesStatus — GitHub이 자동 리다이렉트하지만, 새 클론/링크는 `KRGameCompanyStatus` 사용 권장)

## 🎮 라이브 대시보드
**https://hazelryu.github.io/KRGameCompanyStatus/dashboard/**

15개사 분기/연간 매출 비교 차트(절대값·성장률 토글), 회사별 카드(현재 앱 순위 연동, 출시예정작 하이라이트), 구글플레이·앱스토어 Top100 순위(신규진입/순위변동 표시), PC방·스팀 순위를 한 화면에서 확인할 수 있습니다.

## 데이터
- [`data/companies/`](data/companies/) — Krafton, Nexon, NCSOFT, Kakao Games, Devsisters, Com2uS, Netmarble, NHN, Neowiz, Pearl Abyss, Wemade, Shift Up, Webzen (13개 상장사, 분기 IR) + Smilegate, Haegin (2개 비상장사, 연간 DART) — 매출 추이 + 주요 타이틀 지표 + 출시예정작
- [`data/summary/revenue_trend.csv`](data/summary/revenue_trend.csv) — 15개사 매출·영업이익 통합 비교 CSV
- [`data/app_rankings/`](data/app_rankings/) — 한국 구글플레이·앱스토어 매출 Top100 (주간 갱신) + [원스토어 하이라이트](data/app_rankings/onestore.md)
- [`data/pc_rankings/`](data/pc_rankings/) — 게임트릭스 PC방 점유율 + 스팀 코리아/글로벌 순위

자세한 구조와 갱신 주기는 [`data/README.md`](data/README.md) 참고.

Last updated: 2026-07-14
