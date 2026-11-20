# Kel Reid
Senior Software Engineer with 12 years of experience specializing in backend architecture, distributed systems, and real-time trading infrastructure. Focused on deterministic state integrity, asynchronous concurrency in Python, and fail-closed operational safeguards.

## Featured Projects

### [Market-Making Trading Engine](https://github.com/kel-reid/Kalshi-Trading-Bot)
An autonomous, event-driven market-making engine for prediction markets, designed and deployed to trade live capital in production.
- **Asyncio Core Loop & Thread Offloading:** Core event loop in Python asyncio manages WebSocket feeds, strategy recalculation, and a token-bucket rate limiter. Offloads blocking I/O (RSA auth signatures and PostgreSQL writes) via `asyncio.to_thread` to maintain sub-second loop responsiveness.
- **Microstructure Pricing & Dynamic Spread Engine:** Adapts the Avellaneda-Stoikov model for binary contracts. Calculates rolling 30-second realized volatility and book depth, hard-floors spreads against Kalshi's quadratic transaction fee curve (`0.07 * P * (1 - P)`), and scales risk aversion ($\gamma$) dynamically with inventory drift.
- **Seasonal Sports Router & Discovery:** Autonomous market selection across thousands of Kalshi listings. Normalizes system time to Eastern Time, prioritizes active league slates by day-of-week (CFB on Fri/Sat, NFL on Sun/Mon/Thu, NBA midweek), and verifies live daily game counts via ESPN's schedule API before probing books.
- **Authoritative State Reconciliation:** In-memory positions update on low-latency WebSocket execution streams. Enforces periodic REST audits against the exchange ledger every five minutes to catch dropped packets and eliminate local inventory drift.
- **Fail-Closed Safeguards:** Implements price-velocity circuit breakers, post-fill quiescence pauses, session loss limits, and OS signal handlers (`SIGINT`/`SIGTERM`) that execute a synchronous kill switch to purge all resting quotes before process exit.
- **Production Infrastructure & Telemetry:** Provisioned on DigitalOcean using Terraform with private VPCs, Doppler secret injection, automated GitHub Actions CI/CD, and custom Prometheus metrics piped into Grafana.

### [DFS Optimizer](https://github.com/kel-reid/DFS-Optimizer)
A Monte Carlo and mathematical optimization engine built to construct high-ceiling daily fantasy sports portfolios for FanDuel and DraftKings.
- Formulates lineup selection as a mixed-integer programming problem in PuLP/CBC under strict salary cap, stacking, exposure, and uniqueness constraints.
- Simulates 5,000 slates using skewed player outcome distributions and correlated team-level shocks in NumPy against an empirical field of 10,000 opponent lineups.
- Solves portfolio selection to maximize risk-adjusted tournament payoff within configurable per-position exposure limits.
- Containerized with Docker and tested via pytest.

## Technical Stack
<table>
  <thead>
    <tr>
      <th align="left" valign="top">Languages &amp; Runtimes</th>
      <th align="left" valign="top">Architecture &amp; Systems</th>
      <th align="left" valign="top">Data &amp; Persistence</th>
      <th align="left" valign="top">Infrastructure &amp; Tooling</th>
      <th align="left" valign="top">Observability</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
        Python (asyncio)<br/>
        SQL<br/>
        Bash / Shell
      </td>
      <td valign="top">
        Distributed Systems<br/>
        Real-Time Order Books<br/>
        Market Making Models<br/>
        REST &amp; WebSocket APIs
      </td>
      <td valign="top">
        PostgreSQL<br/>
        Redis<br/>
        NumPy / pandas<br/>
        State Reconciliation
      </td>
      <td valign="top">
        Docker<br/>
        Terraform<br/>
        DigitalOcean / VPC<br/>
        Doppler Secrets<br/>
        GitHub Actions CI/CD
      </td>
      <td valign="top">
        Prometheus<br/>
        Grafana<br/>
        Sentry
      </td>
    </tr>
  </tbody>
</table>

## Get in touch

Find me on [LinkedIn](https://www.linkedin.com/in/kel-reid/),  [X](https://x.com/kel_codes_),  or reach out via email at [kreidva@icloud.com](mailto:kreidva@icloud.com).
