---
name: modern-portfolio-theory
version: "0.1.0"
description: "Modern Portfolio Theory (Markowitz 1952) — 포트폴리오 전체 위험·수익을 최적화. Efficient Frontier, 상관관계 기반 분산, Sharpe 비율. 자산 배분 의사결정의 이론적 출발점."
---

# Modern Portfolio Theory (MPT)

## 한 줄 요약

"얼마나 버는가"가 아니라 **"같은 수익을 얻으면서 얼마나 변동성을 줄이는가"**. 자산 간 **상관관계**를 활용해 *공짜 점심*(분산 이득)을 얻는 것이 MPT의 핵심.

## 이론 기원

- **Harry Markowitz (1952)** — "Portfolio Selection", *Journal of Finance*. 1990 노벨경제학상.
- **William Sharpe (1964)** — CAPM, Sharpe Ratio.
- **James Tobin (1958)** — Separation Theorem, 무위험자산 도입.
- 현대 포트폴리오 이론의 **출발점**. All-Weather, Risk Parity, Factor Investing 모두 MPT의 변주나 확장.

## 핵심 개념

### 1. 기대수익 vs 변동성
- 개별 자산의 수익(E[R])과 변동성(σ) 두 숫자로 요약
- **위험 = 변동성(표준편차)**으로 단순화 — MPT의 가장 큰 단순화이자 한계
- **정규분포 · iid 가정**: 수익률이 정규분포를 따르고 각 기간 독립동일분포라는 전제. 실제 금융시계열은 (1) 자기상관·군집변동성(volatility clustering), (2) 음의 왜도(negative skew), (3) 초과첨도(excess kurtosis, fat tail)를 보임. 2008·2020·2022 같은 6σ+ 사건이 수십 년에 한 번씩 관측.

### 2. 상관관계(ρ)가 마법
- 두 자산 수익이 완벽 동조(ρ=1)면 분산 이득 없음
- **ρ < 1이면 포트폴리오 변동성이 가중평균보다 낮음** — 수학적으로 증명됨
- 음의 상관(ρ<0) 자산 조합이 가장 강력

### 3. Efficient Frontier
- "같은 위험에서 최대 수익" 혹은 "같은 수익에서 최소 위험"을 만족하는 포트폴리오들의 곡선
- 이 곡선 *위쪽*은 존재 불가, *아래쪽*은 비효율
- 실전 자산배분은 이 곡선 위의 한 점을 고르는 문제

### 4. Sharpe Ratio
$$\text{Sharpe} = \frac{E[R] - R_f}{\sigma}$$
- 단위 위험당 초과수익. 포트폴리오 평가의 표준 지표
- **정규분포 가정의 함정**: 실제 수익률은 왼쪽 꼬리가 두꺼움(negative skew, excess kurtosis). 같은 Sharpe라도 헤지펀드·옵션매도 전략은 꼬리 손실이 Sharpe에 반영 안 됨 → 과대평가.
- 대안 지표: **Sortino Ratio** (하방 변동성만), **Calmar Ratio** (MDD 기준), **Omega Ratio** (전체 분포 기반). MPT의 Sharpe는 *분포가 정규에 가까울 때만* 신뢰.

### 5. 무위험자산 + 위험자산 조합 (Capital Market Line)
- 무위험자산(현금·국채)과 접선 포트폴리오를 섞으면 Frontier보다 더 좋아짐
- 레버리지·디레버리지로 위험 수준을 스케일링

## 언제 쓰나

- "주식:채권:금 비중 어떻게 잡지?" — 자산군 배분 의사결정
- "한 자산에 몰빵해도 돼?" 반박 논리
- 기존 포트폴리오의 Sharpe 비율 평가
- 새 자산 추가 시 *상관관계로 분산 이득이 생기는지* 체크
- 기관 투자자 IPS(Investment Policy Statement)의 이론적 기반

## 실전 적용

```
1. 자산군 정의 (5~10개)
   예: 한국주식, 해외주식(선진), 해외주식(신흥), 한국채권, 해외채권, 금, REITs, 현금
2. 각 자산의 기대수익·변동성·상관관계 추정
   - 과거 10~20년 데이터가 출발점 (하지만 미래 예측 아님)
3. Efficient Frontier 시뮬레이션
   - 엑셀·Python(pandas, scipy.optimize)·온라인 툴(Portfolio Visualizer)
4. 자신의 위험감내 수준에 맞는 점 선택
   - 변동성 10% 이하? 15%? 20%?
5. 월/분기 단위로 실제 수익·변동성 체크, 이론과 괴리 크면 가정 재검토
```

## 한국 맥락

### 한국 투자자의 MPT 적용 주의점
- **KOSPI·코스닥은 미국·유럽 주식과 상관 높음** (글로벌화). 순수 "국내주식" 분산 효과 제한적.
- **원화자산 편향(home bias)** — 한국 투자자 자산 80%+가 원화. 환헤지 관점에서 해외자산은 이미 *분산*에 기여.
- **부동산 비중이 포트폴리오의 실세**: 평균 한국 가계 자산의 70%+가 부동산. MPT 계산에서 빼면 현실과 괴리.
- **채권 접근성**: 미국 국채 ETF(TLT, IEF)는 원화 투자자에게 환 리스크 포함됨. KODEX 국고채 등 원화 채권 ETF와 구분.
- **금투세·배당세**: 세후 수익률 기준으로 Sharpe를 재계산해야 한국 현실.

### 한국 투자자를 위한 일반적 프레임 (추천 아님, 예시)
- 공격형(20·30대): 해외주식 60 / 국내주식 20 / 금·REITs 10 / 현금·채권 10
- 균형형(40대): 해외주식 40 / 국내주식 15 / 채권 25 / 금·대체 10 / 현금 10
- 보수형(50대+): 해외주식 25 / 국내주식 10 / 채권 45 / 금 10 / 현금 10
- 위는 *예시*이며 부동산·퇴직금·국민연금을 포함한 전체 자산 맥락에서 재계산해야 한다.

## 안티패턴 & 과적용

- **과거 데이터로 미래를 그대로 예측** — 10년 Sharpe가 1.2라고 앞으로도 1.2 아님
- **Efficient Frontier 정확도 믿기** — 입력 5% 오차 → 출력 30% 차이 (모델 민감도 극심)
- **상관관계가 정적이라는 가정** — 위기 시 상관관계 모두 1로 수렴 (분산 효과 사라짐)
- **변동성 = 위험이라는 단순화** — 상승 변동성도 "위험"으로 계산됨. 꼬리 리스크 미반영.
- **개별 종목 수준 적용** — MPT는 자산군 배분에 유용, 종목 10개 선택엔 부적합
- **재계산 강박** — 매월 Frontier 다시 돌리고 비중 조정하면 거래비용·세금으로 이득 상쇄

## 한계

1. **정규분포 가정** — 실제 수익률은 fat tail. 극단 사건을 과소추정.
2. **과거 = 미래 가정** — 체제 전환(금리·인플레·지정학)에 취약.
3. **변동성 = 위험 가정** — Taleb이 가장 강하게 비판. 진짜 위험은 영구 손실.
4. **거래비용·세금 무시** — 이론엔 없지만 실전에선 결정적.
5. **투자자 효용이 평균-분산 효용이라는 가정** — 실제 인간은 손실회피·후회회피 편향 (→ `behavioral-biases`).
6. **입력값 민감도** — 기대수익 입력이 약간만 틀려도 최적해가 크게 바뀜 (Michaud의 "error maximization" 비판).

## 현대 MPT 진전 (참고)

Markowitz 원론의 한계를 보완한 현대 기법:

- **Black-Litterman 모델 (1990)**: CAPM 균형 수익률을 사전분포로, 투자자 view를 posterior로 결합. 입력 민감도·극단 비중 문제 완화.
- **Resampled Efficient Frontier (Michaud 1998)**: 몬테카를로로 여러 frontier 평균. 안정적 비중.
- **Risk Parity** (→ `all-weather`): 기대수익 추정 의존 제거.
- **Hierarchical Risk Parity (López de Prado 2016)**: 머신러닝 클러스터링으로 상관구조 계층화. 전통 MPT의 역행렬 불안정 문제 회피.
- **Robust Optimization**: 입력 불확실성을 명시 제약으로 내재화.

개인 투자자 시사점: Efficient Frontier 소프트웨어의 결과를 *최적*으로 받아들이지 말 것. 현대 연구자들도 MPT 원론을 그대로 쓰지 않는다.

## 이 프레임워크와 함께 쓰는 것들

- `all-weather` — MPT의 상관관계 철학을 경제 체제별로 재구성한 응용
- `bogleheads` — MPT를 최소 비용·3펀드로 단순화한 실천판
- `factor-investing` — MPT의 기대수익 설명을 팩터로 분해한 확장
- `rebalancing` — MPT가 지정한 비중을 유지하는 실행 메커니즘

## 이 프레임워크가 *틀렸을 때*

- 꼬리 리스크·블랙스완 대비 → `barbell-strategy`
- 행동·심리 문제 → `behavioral-biases`
- 개별주 저평가 찾기 → `value-investing`
- 한국 세후 수익률 → `korean-tax-optimization`
- 매수 타이밍 분할 → `dollar-cost-averaging`

## 추가 학습

- Markowitz, H. (1952). "Portfolio Selection." *Journal of Finance*.
- Bernstein, W. *The Intelligent Asset Allocator* (2000). — MPT 대중서 걸작.
- Swensen, D. *Pioneering Portfolio Management* (2000). — 예일대 기금 적용.
- 온라인: Portfolio Visualizer (portfoliovisualizer.com) — Efficient Frontier 시뮬레이션 무료.
- 비판: Taleb *The Black Swan* — MPT 한계의 대표적 비판서.
