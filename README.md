# Investment Framework

개인 투자 의사결정을 위한 메타 라우터 + 프레임워크 컬렉션. 포트폴리오 이론·시스템 규율·행동 편향·한국 세제·FIRE 등 12개 프레임워크를 하나의 라우팅 레이어에 묶는다.

## 설계 원칙

1. **이론 복붙 금지, 한국 맥락으로 번역** — Markowitz·Bogle·Dalio·Taleb 등 영미권 프레임을 전세·ISA·연금저축·건보료 같은 한국 제도 위에 다시 얹는다.
2. **종목 추천기가 아니다** — 어떤 종목·펀드를 사라고 말하지 않는다. *의사결정 구조*만 다룬다.
3. **과적용 경고 필수** — 모든 프레임워크는 단점·한계·틀리는 조건을 동일 비중으로 적는다.
4. **행동 편향 전제** — 최적 전략보다 *지킬 수 있는 전략*이 우선. Kelly와 MPT가 수학적으로 옳아도 패닉 매도하면 무의미.

## 구조

```
investment-framework/
├── SKILL.md                     # 메타 라우터 — 상황 → 프레임워크 선택
├── modern-portfolio-theory/     # Markowitz, 분산투자 수학
├── all-weather/                 # Ray Dalio, 경제 4분기 risk parity
├── bogleheads/                  # Bogle, 3-fund 저비용 인덱스
├── barbell-strategy/            # Taleb, 안전 + 극고위험 양극
├── value-investing/             # Graham/Buffett, 내재가치·안전마진
├── factor-investing/            # Fama-French, 팩터 프리미엄
├── dollar-cost-averaging/       # 정액 분할매수
├── rebalancing/                 # 주기·밴드 리밸런싱
├── behavioral-biases/           # Kahneman/Thaler, 편향 대응
├── kelly-criterion/             # 최적 베팅 사이즈
├── korean-tax-optimization/     # ISA·연금저축·IRP·양도세·배당세
└── fire-korean/                 # 한국형 FIRE 경로
```

## 사용

```
/money <상황 설명>
```

메타 라우터가 신호를 매핑해 1~3개 프레임워크를 선택, Skill 툴로 실행·합성한다.

## 범위 바깥

- 개별 종목·펀드 추천
- 시장 전망·예측 (언제 오를지)
- 단기 매매·트레이딩 시그널
- 부동산 (→ [`realty`](https://github.com/ironyjk/real-estate-framework))
- 사업 전략 (→ `think`)
- 심리·감정 상담 (→ `counsel`)

## 자매 레포

자산 배분 관점에서 주식·채권·현금 + 부동산을 함께 놓고 판단해야 하는 상황(예: "목돈 5억 들어왔는데 집 살까 ETF 담을까")은 [`real-estate-framework`](https://github.com/ironyjk/real-estate-framework)(`/realty`)와 함께 쓰는 것을 권장.

## 메타

- `last_verified: 2026-04-17`
- `valid_until: 2026-10-17` — 한국 세제(ISA·연금·금투세·배당세)·건보료 산정 기준은 6개월 내 재검증 필요

## 면책

**이 레포는 의사결정 보조 도구이며 투자 자문이 아니다.**

- 특정 종목·ETF·펀드·섹터·비중·매매 타이밍을 추천하지 않는다. 매수·매도 결정은 전적으로 사용자 책임이다.
- 이 레포는 자본시장법상 "유사투자자문업" 영역의 활동(불특정 다수 대상 특정 종목·포트폴리오·시그널 제공)을 하지 않는다. 사고 구조·프레임만 제공한다.
- 한국 세제 관련 내용은 2026-04-17 기준이며 변경될 수 있다. 실제 세무 판단은 세무사·PB와 확인하라.
- 과거 수익률·사이클은 미래를 보장하지 않는다.
- 여기 적힌 모든 프레임워크는 *틀릴 수 있는 모형*이다. 현실이 모형과 다르면 현실이 맞다.
