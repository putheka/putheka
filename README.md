<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:1e3a8a&height=180&section=header&text=Full-Stack%20Engineer&fontSize=42&fontColor=ffffff&fontAlignY=35&desc=Systems%20·%20APIs%20·%20Test-Driven%20Development&descAlignY=58&descSize=16" width="100%" alt="header" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&pause=1200&color=3B82F6&center=true&vCenter=true&width=620&lines=Tests+first%2C+always.;Typed+contracts%2C+thin+controllers.;Red+%E2%86%92+Green+%E2%86%92+Refactor" alt="typing" />
</a>

<br/>

![Focus](https://img.shields.io/badge/focus-backend%20architecture-0f172a?style=flat-square)
![Method](https://img.shields.io/badge/method-TDD-16a34a?style=flat-square)
![Open to](https://img.shields.io/badge/open%20to-collaboration-3b82f6?style=flat-square)

</div>

---

### Overview

Full-stack engineer. Most of my day goes to the parts users never see: domain modelling, API contracts, third-party integrations, and the test suite that keeps all three honest. I care more about how a system fails than how it demos.

---

### How I work

<table>
<tr>
<td width="50%" valign="top">

**Test-driven by default**

A failing test before the implementation. Feature tests at the HTTP boundary, unit tests for domain logic, no mocking of code I own. Coverage is a diagnostic, not a target.

</td>
<td width="50%" valign="top">

**Typed across the boundary**

Types derived from the API contract, not hand-written twice. A schema change should break the build, not production.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Thin controllers, fat domain**

Requests validate, controllers delegate, actions and services hold behaviour. Data access stays out of the view layer.

</td>
<td width="50%" valign="top">

**Boring infrastructure**

Queues for anything slow, idempotent jobs, structured logs. Third-party services treated as unreliable by default.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Readable over clever**

Naming, small functions, obvious control flow. If a change needs a comment to explain why it's safe, the design is wrong.

</td>
<td width="50%" valign="top">

**Migrations you can reverse**

Schema changes shipped in steps: add, backfill, switch, drop. Never a deploy that can't be rolled back.

</td>
</tr>
</table>

---

### Currently

- Designing and hardening REST APIs for production traffic
- Integrating commerce and payment providers with unreliable upstreams
- Improving test speed and reliability in a large, long-lived codebase
- Reading more on domain-driven design and safely refactoring legacy code

---

<details>
<summary><b>📊 GitHub activity</b></summary>
<br/>

<div align="center">

<!-- Replace GH_USER with your GitHub handle -->
<img height="165" src="https://github-readme-stats.vercel.app/api?username=GH_USER&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&hide=issues" alt="stats" />

<br/><br/>

<img src="https://streak-stats.demolab.com?user=GH_USER&theme=tokyonight&hide_border=true" alt="streak" />

<br/><br/>

<img src="https://github-profile-trophy.vercel.app/?username=GH_USER&theme=nord&no-frame=true&no-bg=true&column=7&margin-w=8" alt="trophies" />

</div>
</details>

<details>
<summary><b>📌 Selected work</b></summary>
<br/>

| Project | What it solves |
|---|---|
| _project-one_ | The problem it removed, in one line — not the feature list |
| _project-two_ | What became possible that wasn't before |
| _project-three_ | The interesting constraint you designed around |

> Replace with real repositories. Two well-documented projects beat ten empty ones.

</details>

<details>
<summary><b>🧪 What a test looks like to me</b></summary>
<br/>

The assertion I care about most is rarely the status code:

```
it rejects an order when stock is insufficient
  → request returns a validation error
  → the error names the offending field
  → and the stock row is unchanged
```

A rejected request that silently mutated state is a passing test and a broken system.

</details>

---

<div align="center">

<sub>Open to collaborating on backend architecture, API design, and testing infrastructure.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1e3a8a,100:0f172a&height=100&section=footer" width="100%" alt="footer" />

</div>
