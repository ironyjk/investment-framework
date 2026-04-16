---
name: kelly-criterion
version: "0.1.0"
description: "Kelly Criterion (John L. Kelly Jr., 1956) — 장기 자산 성장률을 최대화하는 베팅 비중 공식. Fractional Kelly(1/2, 1/4)로 변동성 완화. 파산 확률 관리. 포지션 사이징의 수학적 기준."
---

# Kelly Criterion

## 한 줄 요약

**"얼마를 베팅할까"**의 수학적 답. 장기 로그 성장률을 최대화하는 최적 비중. 실전에선 **Fractional Kelly (1/2, 1/4)**로 낮춰 변동성과 파산 확률을 관리. *포지션 사이징의 기본기*.

## 이론 기원

- **John L. Kelly Jr. (1956)** — Bell Labs 엔지니어. "A New Interpretation of Information Rate". 정보이론 응용.
- **Edward O. Thorp** — *Beat the Dealer* (1966), *Beat the Market* (1967). Kelly를 블랙잭·주식에 적용. 퀀트 투자의 선구자.
- **Claude Shannon** — Kelly와 함께 주식 적용 실험. 초창기 퀀트.
- **William Poundstone** — *Fortune's Formula* (2005). Kelly 이야기 대중 저작.

## 핵심 공식

### 1. 기본 Kelly 공식 (이진 결과, 독립 반복 베팅)

$$f^* = \frac{bp - q}{b}$$

- $f^*$: 자본의 최적 베팅 비율
- $b$: 이길 때 배당률 (순이익/베팅금)
- $p$: 이길 확률
- $q = 1 - p$: 질 확률
- **가정**: 베팅 결과가 독립·동일분포(iid), 원금의 임의 비율 베팅 가능(무한분할), 무한 반복. 이 가정 깨지면 공식 최적성 상실.

### 2. 주식·투자 일반화 (Merton 연속시간 버전)

$$f^* = \frac{\mu - r}{\sigma^2}$$

- $\mu$: 기대수익률
- $r$: 무위험수익률
- $\sigma^2$: 분산(변동성 제곱)
- **전제**: 가격이 기하브라운운동(GBM)을 따르고, 투자자 효용이 **로그효용(log-utility, CRRA=1)**일 때 성립. Merton(1969) 최적소비-투자 문제의 특수해.
- **일반 CRRA 효용** ($U(W) = W^{1-\gamma}/(1-\gamma)$)에선 $f^* = (\mu-r)/(\gamma \sigma^2)$. 일반 투자자는 $\gamma \approx 2\sim 4$로 Kelly의 **1/2 ~ 1/4**가 자연스러운 효용함수 최적해.
- **Samuelson 비판(1979, "Why we should not make mean log of wealth big")**: 로그효용은 *특별한* 효용함수일 뿐 보편적 기준이 아니다. Kelly를 "기하평균 최대화"로 자연법칙처럼 받아들이면 안 됨.

### 3. 로그 성장률 (Kelly가 최대화하는 것)

$$G = p \ln(1 + bf) + q \ln(1 - f)$$

- **산술평균 수익**이 아닌 **기하평균 수익** 최대화
- 장기 누적 자산 성장의 기준

### 4. Full Kelly의 문제

- 단기 drawdown 크고 변동성 매우 높음
- 파라미터 추정 오차에 민감 (기대수익 10% 틀리면 결과 크게 바뀜)
- 실전에선 **½ Kelly** 또는 **¼ Kelly** 사용

## 핵심 통찰

### 1. 우위(edge)가 있어야 적용 의미 있음

- $\mu < r$ (기대수익이 무위험보다 낮음)이면 $f^* < 0$ = 공매도해야 Kelly 최적
- 우위 없는 사람이 Kelly 쓰면 파산 가속

### 2. Fractional Kelly가 실전 표준

- ½ Kelly: 기하평균 성장률의 75% 유지 + 변동성 50% 감소
- ¼ Kelly: 성장률 44% 유지 + 변동성 75% 감소
- 대부분 상황에서 ½ 또는 ¼ Kelly가 합리적

### 3. 파산 확률(ruin risk)

- Full Kelly는 *이론상* 파산 안 함 (무한히 분할 베팅 가정)
- 실전은 이산·유한 → 파산 확률 존재
- Fractional이 파산 확률을 극적으로 낮춤

### 4. Kelly vs 효용이론

- Kelly는 log-utility 투자자에게 최적
- 대부분 인간은 log-utility보다 보수적 (손실회피)
- → Fractional Kelly가 심리적으로 지속 가능

## 언제 쓰나

- **개별 베팅 사이즈 결정** — 한 종목에 얼마 할당
- **레버리지 한계** — 최대 레버리지 배율 결정
- **옵션·파생 포지션 사이징**
- **자동매매 봇 1회 거래 크기**
- **집중 투자 전략의 상한 설정**
- 체계적 트레이딩 전략(승률·손익비 추정 가능할 때)

## 실전 적용

### 예시 1: 주식 기대수익·변동성 기반

```
가정:
- 주식 포트폴리오 기대수익 μ = 8%
- 무위험수익률 r = 3%
- 변동성 σ = 18%

Full Kelly:
f* = (0.08 - 0.03) / 0.18² = 0.05 / 0.0324 ≈ 154%

→ 1.54배 레버리지가 Full Kelly (!!)
→ 대부분 투자자에게 말도 안 되게 공격적
→ ¼ Kelly: 38% (즉 레버리지 없이 주식 38%)
```

### 예시 2: 이진 베팅 (투기적)

```
가정: 70% 확률로 2배 이익, 30% 확률로 전액 손실
b = 1, p = 0.7, q = 0.3

f* = (1 × 0.7 - 0.3) / 1 = 40%

→ Full Kelly: 자산의 40% 베팅
→ ½ Kelly: 20%
→ ¼ Kelly: 10%
```

### 예시 3: 자동매매 봇 (kisdev 맥락, SOXL 3x 레버리지)

```
가정: SOXL (반도체 3x 레버리지 ETF) 자동매매 봇
- 백테스트 월 기대수익 3%, 월 변동성 10% (연 σ≈35%)
- 월 평균 거래 20회, 승률 55%, 평균 손익비 1.3

주의: SOXL은 이미 3x 레버리지 자산 — Kelly 계산 시 σ를
기초자산(SOX)의 3배로 봐야 하며, 일일 리밸런싱 감쇠(volatility drag)로
장기 기대수익이 기초자산의 3배가 아님.

연 기준 Kelly 추정:
μ(연) ≈ 3% × 12 = 36% (백테스트 과신 위험)
σ(연) ≈ 10% × √12 ≈ 35%
r ≈ 3%
Full Kelly = (0.36 - 0.03) / 0.35² ≈ 2.7x 레버리지

→ 이미 SOXL이 3x이므로 Full Kelly = 추가 레버리지 없음 전제
→ 백테스트 오버피팅 고려: μ를 절반(18%)으로, σ는 1.5배(50%)로
   보수적 재계산 → f* = (0.18-0.03)/0.25 = 60%
→ ¼ Kelly = 15% → 총 자산의 15%만 SOXL 봇에 배분
→ kisdev $8K가 전체 자산($80K+ 가정)의 10% 내외면 Barbell·Kelly 양쪽 일관
```

**원금 증액 판단 체크리스트**:
1. 실거래 샤프비율이 백테스트의 60% 이상인가 (일반적 감쇠 반영)
2. 3년 이상 실거래에서 최대 drawdown이 허용 범위(예: 전체 자산의 5%) 내인가
3. 사용자 맥락: 자녀 3 · 울산 갈아타기 자금 · 1.8억 근로소득 — 이 돈이 0이 되어도 라이프 플랜 유지 가능한가 (Barbell 공격 파트 조건)
4. 증액 시 Kelly 계산값의 **¼**만 추가 (예: $8K → $10K 점진)

## 한국 맥락

### 1. 한국 투자자에게 Kelly가 위험한 이유

- **파라미터 추정 어려움**: μ·σ를 정확히 모름. 과거 데이터로는 미래 Full Kelly 과대추정 흔함.
- **단일 자산 과집중 유혹**: Full Kelly 적용하면 한 종목에 40~80% 가능. 분산 원칙과 충돌.
- **레버리지 문화**: 한국의 신용거래·미수 문화는 Kelly를 파산 가속으로 왜곡
- **세금 미반영**: 세후 기대수익 기준으로 재계산해야 함

### 2. 한국 투자자용 Kelly 사용 가이드

- **Full Kelly 절대 금지** — 추정 오차 고려하면 실제 Kelly는 계산값의 절반 이하
- **¼ Kelly를 기본**으로 + 개별 종목엔 더 보수적 (⅛ Kelly 이하)
- **레버리지 사용은 ½ Kelly 미만**으로 제한
- **자동매매 봇**: 백테스트 오버피팅 고려해 계산값의 30~50%만 사용

### 3. kisdev(SOXL 봇) 케이스 연결

- 월 100만 원 적립 + $8K 운용 현재 구조
- Full Kelly 계산값을 실제 포지션으로 쓰지 말 것
- 백테스트 기대수익의 ½ 정도로 conservative μ 가정
- σ는 실제 백테스트의 1.5배로 보수적 가정
- 사용자 노트: "원금/파라미터 최적화 방향"이라면 Kelly가 원금 스케일링 상한을 정하는 기준이 될 수 있음

## 안티패턴 & 과적용

- **Full Kelly 사용** — 추정 오차 고려 없음, 파산 가속
- **이길 확률 과대평가** — p=0.55인데 0.70으로 가정해 Kelly 계산
- **독립 베팅 아닌데 독립 가정** — 여러 종목이 같은 팩터에 노출되면 Kelly 분산 의미 감소
- **레버리지 없이 Full Kelly 따라 몰빵** — 한 종목에 80% 자산
- **손실 후 복구 몰빵** — 손실 회복용 베팅 증대는 Kelly와 정반대 방향
- **Kelly = 수익률 극대화 착각** — Kelly는 기하평균 최대화. 산술평균·Sharpe와 다름.
- **단기 승률 과신** — 10회 거래로 승률 계산 → 모두 우연. 최소 수백 회 필요.

## 한계

1. **파라미터 추정 불가능성** — 실제 μ·σ·p·b는 미래 값이라 알 수 없음. Kelly는 *이론값에만 최적*.
2. **추정 오차에 극도로 민감** — 입력 10% 오차 → Kelly 30%+ 오차
3. **단기 drawdown 크게 발생** — Full Kelly 자산의 50% 하락이 흔함
4. **심리적으로 지속 불가능** — "수학적 최적"이어도 실제로 못 버팀
5. **이산·유한 가정 위반** — 연속 시간 가정 위반하면 파산 확률 발생
6. **독립성 가정** — 금융시장은 자기상관·체제변화 존재, Kelly 가정 위반
7. **세금·거래비용 미반영** — 실제 수익률 크게 다름
8. **로그효용 특수성 (Samuelson 비판)**: Kelly는 로그효용자의 최적이지 보편 최적이 아님. CRRA 계수 γ=2~4인 평균적 투자자에겐 1/γ Kelly(=1/2~1/4 Kelly)가 효용 극대.
9. **누적분포의 멱법칙성** — 실제 금융시장 수익률은 fat-tailed. Kelly 수식은 정규·로그정규 가정을 써서 꼬리 손실 과소평가.

## 이 프레임워크와 함께 쓰는 것들

- `barbell-strategy` — Barbell의 공격 파트 사이즈 결정
- `value-investing` — 개별 종목 집중 투자 시 상한
- `behavioral-biases` — 과신·도박성 편향 수학적 제어
- `modern-portfolio-theory` — MPT는 평균-분산, Kelly는 기하평균. 보완 관계.

## 이 프레임워크가 *틀렸을 때*

- 분산 투자 기반(Bogleheads) → Kelly 거의 불필요
- 장기 자산배분 문제 → `modern-portfolio-theory` / `all-weather`
- 심리 문제 → `behavioral-biases`
- 매수 타이밍 → `dollar-cost-averaging`

## 추가 학습

- Kelly, J. L. (1956). "A New Interpretation of Information Rate." *Bell System Technical Journal*.
- Thorp, E. (1969). "Optimal Gambling Systems for Favorable Games."
- Poundstone, W. (2005). *Fortune's Formula*. — 대중서.
- MacLean, Thorp, Ziemba (2011). *The Kelly Capital Growth Investment Criterion*. — 학술 컴필레이션.
- Hsu (2008). "Kelly and Half-Kelly for Common Investors" — fractional 근거.
- 비판: Paul Samuelson의 Kelly 비판 논문들 — "Why we should not make mean log of wealth big".
