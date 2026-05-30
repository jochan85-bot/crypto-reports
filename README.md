# MacTrader · Crypto V7 Live

매일 09:00 KST에 산출되는 통합 크립토 시그널(V7) 라이브 차트와 누적 데이터.

- **라이브 차트:** https://jochan85-bot.github.io/crypto-reports/
- **데이터:** `data/history.json` (매일 1행 append)
- **시그널 로직:** [openclaw/workspace/crypto_signal](https://github.com/) — V7 (BTC 사이클 기준 통합, 연속 점수)

## 표시 항목

- BTC/ETH 가격 (KRW)
- 연속 통합 점수 (`-10 ~ +10`, 매수/매도 컷트라인 같이 표시)
- 현재 zone 시작일 + 경과일
- zone 변경 마커 + 시그널 로그 패널
- 1주 / 1달 / 1년 / 5년 / 전체 rangeselector + 줌/팬

## 데이터 스키마 (`data/history.json`)

```json
[
  {
    "date": "2026-05-30",
    "btc_krw": 109099000,
    "eth_krw": 2991000,
    "score": 5.8,
    "zone": "HOLD",
    "zone_since": "2026-05-30",
    "zone_days": 1,
    "zone_changed": true,
    "gate": "분할매수",
    "metrics": {"btc_nupl": 0.27, "btc_mvrv_z": 0.66, "puell": 0.8, "mayer": 0.92, "fng": 23},
    "ethbtc": 0.0274,
    "liq_regime": 0,
    "allocation": null
  }
]
```

매일 append-only. 5년 누적해도 200KB 미만.
