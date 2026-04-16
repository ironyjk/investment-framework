---
name: factor-investing
version: "0.1.0"
description: "Factor Investing (Fama-French 3/5 factor) — 초과수익을 소수의 체계적 '팩터'로 설명. Value, Size, Momentum, Quality, Low-Vol. 스마트베타 ETF의 이론적 기반. 개별 종목 분석 대체."
---

# Factor Investing

## 한 줄 요약

개별 종목의 알파는 운이지만, **특정 속성(팩터)을 가진 종목군은 장기 초과수익을 내는 경향**이 있다는 실증 결과. Value·Size·Momentum·Quality·Low-Volatility 등 팩터에 체계적으로 노출시키는 전략. Bogleheads(패시브)와 Value(액티브) 사이의 중간 지점.

## 이론 기원

- **Eugene Fama & Kenneth French (1993)** — 3-factor model. 시장·사이즈·가치로 주식 수익률 ~90% 설명.
- **Fama-French (2015)** — 5-factor model 추가 (Profitability, Investment).
- **Narasimhan Jegadeesh & Sheridan Titman (1993)** — Momentum factor.
- **Robert Haugen, Andrew Ang** — Low-volatility anomaly.
- CAPM(단일 팩터)의 확장. EMH와 호환되면서 이상현상(anomaly) 인정하는 중도적 입장.

## 핵심 팩터

### 1. Market (Beta)
- 시장 전체에 대한 노출. CAPM의 단일 팩터.
- Sharpe(1964)·Lintner(1965) CAPM: $E[R_i] - R_f = \beta_i (E[R_m] - R_f)$. Fama-French는 이 "단일 베타" 설명력의 한계에서 출발.

### 2. Size (SMB: Small Minus Big)
- 소형주가 대형주 대비 장기 초과수익
- 단, 2010년 이후 프리미엄 축소 논쟁

### 3. Value (HML: High Minus Low)
- 낮은 P/B (높은 book-to-market) 주식이 성장주 대비 초과수익
- → `value-investing`의 팩터 버전

### 4. Momentum (MOM)
- 최근 6~12개월 상승한 종목이 다음 6~12개월도 상승 경향
- 단, 반전 시 손실 크고 변동성 높음

### 5. Profitability / Quality
- ROE·ROIC 높고 이익 안정적인 기업이 초과수익
- 5-factor에서 추가됨

### 6. Low Volatility
- 저변동성 주식이 고변동성 주식보다 초과수익 (CAPM과 상충하는 이상현상)
- Betting-Against-Beta (Frazzini-Pedersen)

### 7. Investment
- 자본투자(설비투자·자산 증가) 적은 기업이 초과수익 (5-factor 추가)

## 팩터 프리미엄 사이즈 (참고)

| 팩터 | 연 프리미엄 (미국, 장기) | 변동성 |
|---|---|---|
| Market | 5~6% | 높음 |
| Value | 3~5% | 중 |
| Size | 1~3% | 중 |
| Momentum | 4~8% | 매우 높음 |
| Quality | 3~4% | 낮음 |
| Low-Vol | 2~3% | 낮음 |

- *과거 데이터 기반, 미래 보장 없음. 최근 10년 대부분 팩터 프리미엄 축소.*

## 언제 쓰나

- Bogleheads(시장 인덱스)만으로는 부족하다고 느낄 때
- 개별 종목 분석 시간·능력 없지만 *초과수익은 원할 때*
- 포트폴리오 팩터 노출 진단 (이미 특정 팩터에 과노출은 아닌가)
- 스마트베타 ETF 선택의 기준
- 기관·연기금 수준의 체계 투자

## 실전 적용

### 스마트베타 ETF 예시 (추천 아님 — 각 팩터에 노출되는 대표 상품 학습용)

| 팩터 | 미국 ETF | 국내 ETF (있으면) |
|---|---|---|
| Value | VLUE, IUSV | TIGER 미국가치 |
| Size (Small) | VB, IJR | KODEX 코스닥150 |
| Momentum | MTUM | - (제한적) |
| Quality | QUAL, DGRO | TIGER 미국퀄리티배당 |
| Low-Vol | USMV, SPLV | KODEX 미국S&P500 저변동성 |
| Multi-factor | DFAX, GSLC | - |

### 팩터 포트폴리오 예시 (Equal-weight multi-factor)

```
Total Market: 40%
Value factor: 15%
Quality factor: 15%
Momentum factor: 10%
Small-cap: 10%
Low-vol: 10%
```

### Dimensional Fund Advisors (DFA) / Avantis 접근

- Fama-French 원전 기반 펀드 운용사
- 팩터 tilt 과학적으로 설계, 낮은 비용
- 개인 접근 제한적이지만 철학은 학습 가치

## 한국 맥락

### 1. 한국 시장에서 팩터 유효성
- **Value**: 한국에서 역사적으로 강한 팩터 (코리아 디스카운트 + 가치주 반등기 존재)
- **Momentum**: 한국 증시 변동성 높아 팩터 노이즈 큼
- **Small**: 코스닥 중소형주 과거 초과수익 있으나 최근 축소
- **Quality**: 2020년 이후 상대적으로 유효

### 2. 국내 팩터 ETF 제약

- 종류 제한적 (미국 대비 1/10 수준)
- 보수 상대적으로 높음 (0.3~0.5%)
- 운용 규모 작아 유동성 이슈
- 해외 팩터 ETF 직구 시 환·세제 고려 필요

### 3. 한국 투자자 팩터 전략

- **글로벌 팩터 ETF 직구** + **한국 가치/배당 ETF** 조합
- **밸류업 프로그램 수혜주** = 한국판 Value+Quality 하이브리드
- **중소형주 편향**은 한국에서 유동성·세금(양도세 대주주) 이슈로 제한

## 안티패턴 & 과적용

- **단일 팩터 몰빵** — Value 100% 포트폴리오는 2010~2020 10년간 시장 패배
- **팩터 타이밍** — "지금은 Value 시점" 예측은 일반적으로 실패
- **과거 프리미엄 연장** — 장기 데이터의 팩터 프리미엄이 미래에도 유지된다는 가정 위험
- **"팩터는 무조건 이긴다"** — 팩터도 10~15년 underperform 구간 존재
- **팩터 과다 조합** — 5개, 10개 팩터 섞으면 결국 시장 인덱스와 유사해지며 비용만 증가
- **데이터 마이닝 (Factor Zoo)**: 학술적으로 300+ 팩터가 발견됨, 대부분 실거래로는 재현 안 됨
  - Harvey, Liu, Zhu(2016): t-statistic 임계값을 기존 2.0이 아닌 **3.0 이상**으로 상향해야 진짜 팩터
  - McLean & Pontiff(2016): 학술 발표 후 프리미엄이 평균 **32% 하락**, publication 후 **58%** 하락
  - Bailey & López de Prado(2014): 백테스트 n회 시도 시 유의 p값이 거짓양성일 확률 계산 (deflated Sharpe)
  - **개인 투자자 적용**: 새 팩터·테마 ETF 볼 때 "내가 이 데이터를 수천 번 본 연구자 중 하나인가?"를 먼저 의심

## 한계

1. **팩터 프리미엄 축소 논쟁** — 학술 발표 후 프리미엄이 절반 이상 줄어든다는 연구 (McLean-Pontiff)
2. **거래비용·세금** — 리밸런싱 빈도 높을수록 팩터 프리미엄 잠식
3. **장기 underperform 구간** — Value의 2010년대, Momentum의 2009년 반전 등
4. **단일 국가·기간 편향** — 미국 데이터 중심. 다른 시장·기간엔 약한 팩터 존재.
5. **실행 슬리피지** — 소형주·저유동성 팩터 실제 매매 시 프리미엄 상당 부분 증발
6. **팩터 정의 불일치** — Value를 P/B로 볼지 P/E로 볼지 EV/EBIT로 볼지에 따라 성과 다름

## 이 프레임워크와 함께 쓰는 것들

- `modern-portfolio-theory` — 팩터는 MPT 프레임의 체계적 확장
- `bogleheads` — 팩터 tilt를 추가한 Bogleheads = "Fama-French Boglehead"
- `value-investing` — 가치투자의 정량·체계 버전
- `rebalancing` — 팩터 비중 유지 필수

## 이 프레임워크가 *틀렸을 때*

- 팩터 리서치 시간·관심 없음 → `bogleheads`
- 개별 기업 분석이 목적 → `value-investing`
- 거시 자산배분 문제 → `modern-portfolio-theory` / `all-weather`
- 꼬리 리스크 → `barbell-strategy`

## 추가 학습

- Fama, E. & French, K. (1993). "Common Risk Factors in the Returns on Stocks and Bonds."
- Fama, E. & French, K. (2015). "A Five-Factor Asset Pricing Model."
- Ang, A. (2014). *Asset Management: A Systematic Approach to Factor Investing*. — 종합 교재.
- Asness, C. et al. "Fact, Fiction, and Value Investing" (AQR 리서치).
- 비판: Harvey, Liu, Zhu (2016). "...and the Cross-Section of Expected Returns." — factor zoo 비판.
- 한국 적용: 김영성 *스마트베타* 등 국내 입문서 소수.
