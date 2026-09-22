# Hello, I'm Kel! 👋🏼

I'm a Senior Software Engineer with 12 years of engineering experience, including 6+ years specializing in web applications and native mobile architectures with a focus on render latency optimization, asynchronous data streaming, and offline-resilient systems.

### Core Expertise
- **Web Frontend:** React, TypeScript, Redux, Vite
- **iOS:** Swift, SwiftUI, UIKit, Swift Concurrency, Apple Instruments, Core Data, URLSession, Keychain 
- **Android:** Kotlin, Jetpack Compose, Coroutines & Flow, Android Jetpack, Keystore 
- **Testing:** Cypress, Playwright, Jest, XCTest, JUnit
- **Observability:** Datadog, Sentry
  

## Technical Highlights

**[Event-Driven Trading Infrastructure](https://github.com/kelcodesstuff/Kalshi-Trading-Bot)**

A production-grade event-driven algorithmic trading bot, designed to serve as a reference architecture for zero-trust cloud infrastructure, automated GitOps delivery pipelines, and real-time observability.

- **Infrastructure as Code (IaC):** Orchestrated cloud resource deployment programmatically via **Terraform**, enforcing declarative configurations, structural validation checks, and tag-based associations.

- **Perimeter & Network Security:** Provisioned an isolated **DigitalOcean** VPC network and enforced firewall rules to block unauthorized inbound connections and limit outbound egress strictly to DNS, HTTP/S, and NTP boundaries.

- **Zero-Trust Secrets Management:** Integrated **Doppler** to inject application secrets and RSA cryptographic credentials directly into container memory at startup, eliminating the need to store plaintext keys or configs on the host disk.

- **Container Hardening & Least Privilege:** Engineered **multi-stage Docker builds** to minimize runtime surface areas, executing services under a low-privilege system user while restricting database and telemetry port bindings to prevent public exposure.

- **Observability Pipeline:** Configured a local **Grafana Alloy** telemetry collector to scrape application-level Prometheus metrics (API latency histograms, inventory levels, PnL) and remote-write them directly to Grafana Cloud.

- **Automated GitOps Pipeline:** Programmed a **GitHub Actions** workflow executing automated testing with coverage metrics, terraform validation, security scanning, image publication to GitHub Container Registry (GHCR), and SSH-based remote deployments.
  
**Stack:** DigitalOcean, Terraform, Docker/Compose, GitHub Actions, Grafana Alloy, Doppler Secrets Manager, PostgreSQL, Python.


## Skills

<table style="width: 100%; border-collapse: collapse;">
  <thead>
    <tr>
      <th align="left" valign="top" width="16.6%">Languages</th>
      <th align="left" valign="top" width="16.6%">Frameworks & Libraries</th>
      <th align="left" valign="top" width="16.6%">Testing</th>
      <th align="left" valign="top" width="16.6%">CI/CD & Infrastructure</th>
      <th align="left" valign="top" width="16.6%">Observability</th>
      <th align="left" valign="top" width="16.6%">AI Tooling</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
        TypeScript<br/>
        JavaScript<br/>
        Python<br/>
        Swift<br/>
        Kotlin
      </td>
      <td valign="top">
        React<br/>
        GraphQL<br/>
        Redux<br/>
        TanStack Query<br/>
        Vite
      </td>
      <td valign="top">
        Jest<br/>
        React Testing Library<br/>
        Playwright<br/>
        Cypress<br/>
        XCTest<br/>
        XCUITest<br/>
        JUnit<br/>
        Espresso
      </td>
      <td valign="top">
        GitHub Actions<br/>
        CircleCI
      </td>
      <td valign="top">
        Datadog<br/>
        Prometheus<br/>
        Grafana<br/>
        Sentry
      </td>
      <td valign="top">
        Claude Code<br/>
        Gemini API<br/>
        OpenAI API<br/>
        Model Context Protocol (MCP)
      </td>
    </tr>
  </tbody>
</table>


### 
<p align="center">
  <img width="2752" height="1536" alt="CI-CD" src="https://github.com/user-attachments/assets/8a1c5689-f224-4b69-9710-427c52c3e044" />
</p>
