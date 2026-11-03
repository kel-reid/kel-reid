# Hello, I'm Kel!

I'm a Senior Software Engineer with 12 years of experience specializing in backend architecture, distributed systems, and low-latency infrastructure. I design and scale resilient, concurrent services with strict state integrity, event-driven pipelines, and production-grade observability.

## Projects

### [Market-Making Trading System](https://github.com/kel-reid/Kalshi-Trading-Bot)

An event-driven market-making trading system for prediction markets on Kalshi. Built to manage real capital with a zero-tolerance posture for unhandled state drift, prioritizing capital preservation and fail-closed safety.

- **Concurrency & pricing:** Built in Python asyncio to execute real-time Avellaneda-Stoikov pricing and dynamic inventory hedging against live order books.
- **Market discovery & routing:** Dynamically discovers active markets, spins up isolated worker tasks per contract slate, and tears down execution on settlement.
- **Collateral management:** Tracks balances across exchange shards, routing liquidity from shard 0 and automating sweeps to rebalance capital across contracts.
- **Dual-track state engine:** Combines low-latency WebSocket streams with periodic REST and PostgreSQL reconciliation to guarantee P&L conservation invariants.
- **Fail-closed safeguards:** Enforces price-velocity circuit breakers, post-fill quiescence windows, session loss limits, and an automated SIGTERM kill switch that confirms quote withdrawals before exiting.
- **Infrastructure & observability:** Provisioned on DigitalOcean via Terraform with private VPCs, Doppler secret injection, automated GitHub Actions CI/CD, and Prometheus/Grafana dashboards.


### [DFS Optimizer](https://github.com/kel-reid/DFS-Optimizer)

A Monte Carlo and optimization engine built to generate 150-lineup NFL daily fantasy portfolios for FanDuel and DraftKings.

- Generates 500 candidate lineups with an integer-programming solver (PuLP/CBC) under salary-cap, stacking, exposure and uniqueness constraints.
- Simulates 5,000 slates with skewed player distributions and correlated team-level shocks in NumPy, plus a field of 10,000 opponent lineups, then scores every candidate against that field.
- Selects the 150 lineups with the best simulated return, within per-position exposure caps.
- Detects the target site from its input files and runs the same pipeline for both; tested with pytest; containerized.


## Skills

<table>
  <thead>
    <tr>
      <th align="left" valign="top">Languages</th>
      <th align="left" valign="top">Architecture &amp; Systems</th>
      <th align="left" valign="top">Infrastructure</th>
      <th align="left" valign="top">Observability</th>
      <th align="left" valign="top">Data &amp; Persistence</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
        Python<br/>
        SQL<br/>
        Bash / Shell
      </td>
      <td valign="top">
        Distributed Systems<br/>
        Event-Driven Architecture<br/>
        asyncio / Concurrency<br/>
        REST &amp; WebSocket APIs
      </td>
      <td valign="top">
        Terraform<br/>
        Docker<br/>
        GitHub Actions CI/CD<br/>
        DigitalOcean / VPC<br/>
        Doppler
      </td>
      <td valign="top">
        Prometheus<br/>
        Grafana Cloud / Alloy<br/>
        Sentry
      </td>
      <td valign="top">
        PostgreSQL<br/>
        NumPy / pandas<br/>
        Data Modeling
      </td>
    </tr>
  </tbody>
</table>

## Get in touch

I'm always happy to talk backend systems, reliability or testing. Find me on [LinkedIn](https://www.linkedin.com/in/kel-reid/).
