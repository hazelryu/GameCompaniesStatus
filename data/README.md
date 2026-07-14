# data/ 폴더 안내

라이브 대시보드: **https://hazelryu.github.io/KRGameCompanyStatus/dashboard/** (이 아래 원본 데이터를 사람이 읽기 좋게 시각화한 버전)

## 구조

```
data/
├── companies/          # 회사별 분기/연간 매출 추이 + 주요 타이틀 지표 + 출시예정작 + 공식 IR 링크
│   ├── krafton.md        (상장, KRX 259960)
│   ├── nexon.md          (상장, TSE 3659)
│   ├── ncsoft.md         (상장, KRX 036570)
│   ├── kakaogames.md     (상장, KOSDAQ 293490)
│   ├── devsisters.md     (상장, KOSDAQ 194480)
│   ├── com2us.md         (상장, KOSDAQ 078340)
│   ├── netmarble.md      (상장, KRX 251270)
│   ├── nhn.md            (상장, KOSPI 181710 — 회사 전체 매출, 게임부문 별도 표기)
│   ├── neowiz.md         (상장, KOSDAQ 042420)
│   ├── pearlabyss.md     (상장, KOSDAQ 263750)
│   ├── wemade.md         (상장, KOSDAQ 112040)
│   ├── shiftup.md        (상장, KRX 462870)
│   ├── webzen.md         (상장, KOSDAQ 069080)
│   ├── smilegate.md      (비상장 — DART 감사보고서 기반)
│   ├── haegin.md         (비상장 — DART 감사보고서 기반)
│   └── linegames.md      (비상장 — 리서치는 유지하나 2026-07-14부로 대시보드 표시에서는 제외)
├── summary/
│   └── revenue_trend.csv   # 15개사 분기/연간 매출·영업이익 비교용 통합 CSV
├── app_rankings/
│   ├── latest.md          # 구글플레이·앱스토어 KR 매출 Top100 (주간 갱신, 덮어쓰기)
│   ├── history.csv         # 날짜별 순위 누적 이력 (Top20 구간, 주간 추가)
│   └── onestore.md         # 원스토어 — 전체 차트 비공개라 개별 1위 달성 뉴스만 기록
└── pc_rankings/
    └── latest.md           # 게임트릭스 PC방 점유율 Top10 + 스팀 코리아/글로벌 순위
```

## 갱신 주기
- **companies/*.md, summary/revenue_trend.csv**: 각사 분기 실적 발표 시점마다 (연 4회 내외, 회사별 발표일 상이) — 매주 예약 작업이 신규 발표 여부를 점검
- **app_rankings/, pc_rankings/**: 매주 갱신 (2026-07-14부로 일간→주간 전환, 대신 Top20→Top100으로 범위 확장)

## 비상장사(Smilegate, Haegin, LINE Games) 관련 안내
분기 IR 발표가 없는 회사들입니다. 대신 한국 「외부감사대상법인」 의무에 따라 DART(전자공시시스템)에 제출되는 연간 감사보고서를 언론이 인용한 수치를 사용했습니다. 따라서:
- 분기 단위가 아닌 **연간 단위** 데이터만 존재
- 타이틀별 매출/MAU 등 세부 지표는 대부분 공시되지 않아 "비공개/데이터 없음"으로 표기
- 각 파일 내 수치는 1차 DART 원문이 아닌 2차 언론보도 인용임을 명시 (교차검증한 경우 그 사실도 표기)
- LINE Games는 2026-07-14 대시보드 개편 시 회사 카드 표시에서 제외됨(리서치 파일 자체는 유지) — 필요시 요청해서 다시 노출 가능

## Top100 순위 데이터 관련 안내
- App Store 1~100위, Google Play 1~50위는 **MobileIndex** 실시간 차트 기준(동일 방법론)
- **Google Play 51~100위만 AppBrain**(3rd-party, 별도 산정방식)으로 보충 — 1~50위와 완전히 같은 기준선이 아님
- 51위 이하 구간은 장르·출시연도·누적매출·MAU 컬럼이 아직 수집되지 않아 "—"로 표기
- 순위변동(▲▼)은 2026-07-13 최초 스냅샷(Top20)과 비교한 것만 가능 — 그 외는 "최초수집"

## 데이터 정확성에 대하여
모든 수치는 각 회사 공식 IR 자료 또는 이를 인용한 국내 언론 보도를 출처로 하며, 각 파일 하단에 출처 URL을 명시했습니다. 앱 순위는 모바일인덱스(IGAWorks)/AppBrain의 추정치 기반으로, 실제 플랫폼 공식 수치와 다를 수 있습니다.
