# Kelly Criterion -- Theoretical Foundation

## One-Line Summary

The mathematical answer to **"How much should I bet?"** The optimal fraction that maximizes long-term log growth rate. In practice, use **Fractional Kelly (1/2, 1/4)** to manage volatility and ruin probability. *The fundamentals of position sizing*.

## Theoretical Origins

- **John L. Kelly Jr. (1956)** — A Bell Labs engineer. "A New Interpretation of Information Rate." An application of information theory.
- **Edward O. Thorp** — *Beat the Dealer* (1966), *Beat the Market* (1967). Applied Kelly to blackjack and stocks. A pioneer of quantitative investing.
- **Claude Shannon** — Experimented with Kelly in stocks alongside Kelly himself. An early quant.
- **William Poundstone** — *Fortune's Formula* (2005). A popular account of the Kelly story.

## Core Formulas

### 1. Basic Kelly Formula (Binary Outcome, Independent Repeated Bets)

$$f^* = \frac{bp - q}{b}$$

- $f^*$: Optimal fraction of capital to bet
- $b$: Payoff odds when winning (net profit / amount bet)
- $p$: Probability of winning
- $q = 1 - p$: Probability of losing
- **Assumptions**: Bet outcomes are independent and identically distributed (iid), arbitrary fractions of principal can be bet (infinitely divisible), and bets are infinitely repeated. When these assumptions break down, the formula loses its optimality.

### 2. Generalization for Stocks/Investment (Merton's Continuous-Time Version)

$$f^* = \frac{\mu - r}{\sigma^2}$$

- $\mu$: Expected return
- $r$: Risk-free rate
- $\sigma^2$: Variance (squared volatility)
- **Premise**: Holds when prices follow geometric Brownian motion (GBM) and investor utility is **log utility (log-utility, CRRA=1)**. A special-case solution of Merton's (1969) optimal consumption-investment problem.
- **General CRRA utility** ($U(W) = W^{1-\gamma}/(1-\gamma)$) gives $f^* = (\mu-r)/(\gamma \sigma^2)$. For an average investor with $\gamma \approx 2\sim 4$, **1/2 ~ 1/4 Kelly** emerges naturally as the utility-maximizing optimum.
- **Samuelson's critique (1979, "Why we should not make mean log of wealth big")**: Log utility is merely a *special* utility function, not a universal criterion. One should not accept Kelly as "geometric-mean maximization" as though it were a law of nature.

### 3. Log Growth Rate (What Kelly Maximizes)

$$G = p \ln(1 + bf) + q \ln(1 - f)$$

- Maximizes the **geometric-mean return**, not the **arithmetic-mean return**
- The benchmark for long-term cumulative asset growth

### 4. The Problem with Full Kelly

- Short-term drawdowns are large and volatility is very high
- Highly sensitive to parameter estimation error (a 10% error in expected return produces dramatically different results)
- In practice, use **½ Kelly** or **¼ Kelly**

## Core Insights

### 1. Application Only Makes Sense When You Have an Edge

- If $\mu < r$ (expected return is lower than the risk-free rate), then $f^* < 0$ = Kelly optimality requires going short
- A person without an edge using Kelly accelerates ruin

### 2. Fractional Kelly Is the Practical Standard

- ½ Kelly: Retains 75% of geometric growth rate + cuts volatility by 50%
- ¼ Kelly: Retains 44% of growth rate + cuts volatility by 75%
- In most situations, ½ or ¼ Kelly is reasonable

### 3. Ruin Risk

- Full Kelly *in theory* never goes bankrupt (assumes infinitely divisible betting)
- In practice, betting is discrete and finite → ruin probability exists
- Fractional Kelly dramatically reduces ruin probability

### 4. Kelly vs. Utility Theory

- Kelly is optimal for a log-utility investor
- Most humans are more conservative than log-utility (loss aversion)
- → Fractional Kelly is psychologically sustainable

