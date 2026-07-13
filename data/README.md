# data/ 폴더 안내

## 구조

```
data/
├── companies/          # 회사별 분기 매출 추이 + 주요 타이틀 매출/MAU 등 지표
│   ├── krafton.md       (상장, KRX 259960)
│   ├── nexon.md         (상장, TSE 3659)
│   ├── ncsoft.md        (상장, KRX 036570)
│   ├── kakaogames.md    (상장, KOSDAQ 293490)
│   ├── devsisters.md    (상장, KOSDAQ 194480)
│   ├── linegames.md     (비상장 — DART 감사보고서 기반)
│   ├── smilegate.md     (비상장 — DART 감사보고서 기반)
│   └── haegin.md        (비상장 — DART 감사보고서 기반)
├── summary/
│   └── revenue_trend.csv   # 8개사 분기/연간 매출·영업이익 비교용 통합 CSV
└── app_rankings/
    ├── latest.md         # 최신 구글플레이·앱스토어 KR 매출 Top 20 (매일 갱신, 덮어쓰기)
    └── history.csv       # 날짜별 순위 누적 이력 (매일 추가)
```

## 갱신 주기
- **companies/*.md, summary/revenue_trend.csv**: 각사 분기 실적 발표 시점마다 갱신 (연 4회 내외, 회사별 발표일 상이)
- **app_rankings/**: 매일 갱신

## 비상장사(LINE Games, Smilegate, Haegin) 관련 안내
세 회사는 상장사가 아니므로 분기 IR 발표가 없습니다. 대신 한국 「외부감사대상법인」 의무에 따라 DART(전자공시시스템)에 제출되는 연간 감사보고서를 언론이 인용한 수치를 사용했습니다. 따라서:
- 분기 단위가 아닌 **연간 단위** 데이터만 존재
- 타이틀별 매출/MAU 등 세부 지표는 대부분 공시되지 않아 "비공개/데이터 없음"으로 표기
- 각 파일 내 수치는 1차 DART 원문이 아닌 2차 언론보도 인용임을 명시 (교차검증한 경우 그 사실도 표기)

## 데이터 정확성에 대하여
모든 수치는 각 회사 공식 IR 자료 또는 이를 인용한 국내 언론 보도를 출처로 하며, 각 파일 하단에 출처 URL을 명시했습니다. 앱 순위는 모바일인덱스(IGAWorks)의 추정치 기반으로, 실제 플랫폼 공식 수치와 다를 수 있습니다.
