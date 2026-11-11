<p align="center">
  <img src="./banner.svg" width="100%" alt="Ramya Rajendra, Business & Process Analyst" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Inter&weight=600&size=20&pause=1300&color=E0A030&center=true&vCenter=true&width=720&lines=From+business+need+to+PRD+to+tech+mapping" alt="From business need to PRD to tech mapping" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ramyarajendra/"><img src="https://img.shields.io/badge/LinkedIn-ramyarajendra-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge" alt="LinkedIn" /></a>
  <a href="mailto:ramyareddy9488@gmail.com"><img src="https://img.shields.io/badge/Email-ramyareddy9488%40gmail.com-EA4335?logo=gmail&logoColor=white&style=for-the-badge" alt="Email" /></a>
  <a href="https://ramya-rajendra.github.io/ramya-portfolio/"><img src="https://img.shields.io/badge/Portfolio-website-1F3A68?logo=githubpages&logoColor=white&style=for-the-badge" alt="Portfolio website" /></a>
  <a href="https://opus4.kobv.de/opus4-fhws/frontdoor/index/index/docId/6594"><img src="https://img.shields.io/badge/Master's_thesis-THWS-E0A030?logo=bookstack&logoColor=white&style=for-the-badge" alt="Master's thesis" /></a>
</p>

<br>

Most companies already know their processes are slow. What they usually don't know is **where** the time goes and **which fix pays off first**. That's the work I like: mapping a process step by step, checking it against the data, and turning it into a short list of changes with a number attached.

I studied Computer Science in India, worked as a junior business analyst, and then did a Master in International Business at THWS in Würzburg. So I'm at home on both sides: talking to the people who run a process, and working with the data behind it.

<br>

## My work

### Group consolidation with real data: Koenig & Bauer

**[group-consolidation-koenig-bauer](https://github.com/ramya-rajendra/group-consolidation-koenig-bauer)** &nbsp;|&nbsp; Excel, Python, ECB exchange rates, SAP Group Reporting mapping

How do the accounts of 40 separate companies turn into one set of group figures? I took Koenig & Bauer, a listed printing press manufacturer from Würzburg, and rebuilt the main consolidation steps from its public 2025 annual report, including currency translation. The part that public data can't explain is documented instead of forced to zero.

```mermaid
flowchart LR
    A["Companies' own equity<br/><b>€752.4m</b>"] --> B["Less parent's investments<br/>€415.9m"]
    B --> C["Plus goodwill<br/>€39.8m"]
    C --> D["Explained<br/><b>€376.3m</b>"]
    D --> E["Published group equity<br/><b>€343.1m</b>"]
    style A fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style B fill:#E0A030,stroke:#B07818,color:#14213D
    style C fill:#5B8DEF,stroke:#1F3A68,color:#FFFFFF
    style D fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style E fill:#12A594,stroke:#0B7C6F,color:#FFFFFF
```

| Finding | |
|---|---|
| Consolidation units | **40**, in 13 currencies |
| Remaining gap, documented | **–€33.2m**, mainly holdings between subsidiaries |
| Loss of the parent vs. the group in 2025 | **–€53.5m** vs. **–€13.5m** |
| US subsidiary growth | **+33%** in USD, only **+18%** in EUR |

<br>

### Zalando app reviews: what users want fixed first

**[zalando-app-review-analysis](https://github.com/ramya-rajendra/zalando-app-review-analysis)** &nbsp;|&nbsp; Python, BigQuery SQL, Power BI, Claude

I tagged 3,000 German Play Store reviews of the Zalando app by theme, sentiment and feature request, checked them against checkout funnel data, and prioritised the fixes with RICE. The top priority became a product requirements document and a [clickable prototype](https://ramya-rajendra.github.io/zalando-app-review-analysis/docs/checkout-prototype/). Personal project, not affiliated with Zalando.

<img src="https://github.com/ramya-rajendra/zalando-app-review-analysis/raw/main/dashboard/dashboard.png" width="100%" alt="Power BI dashboard of Zalando app reviews" />

| Finding | |
|---|---|
| Negative reviews about the app itself | **about 390**, more than any other topic |
| "Bug" complaints really about the redesign | **almost half** |
| Checkout starts not completed | **about 55%**, on every device |
| Top priority after RICE | **A more reliable checkout** |

<br>

### Purchase-to-pay on real company data

**[p2p-real-data-analysis](https://github.com/ramya-rajendra/p2p-real-data-analysis)** &nbsp;|&nbsp; Python, pandas, SQL (DuckDB)

I analysed the BPI Challenge 2019 event log: **1.6 million process steps** from the purchase-to-pay process of a large multinational paint and coatings company, to find out what delays supplier payments.

```mermaid
flowchart LR
    A[Purchase order] --> B[Goods receipt]
    B --> C[Vendor invoice]
    C -- "median 10 days" --> D[Invoice recorded]
    D --> E{Payment block?}
    E -- "27.6% of cases, +10 days" --> F[Manual release]
    E -- "no block" --> G[Paid]
    F --> G
    style A fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style B fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style C fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style D fill:#1F3A68,stroke:#5B8DEF,color:#FFFFFF
    style E fill:#E0A030,stroke:#B07818,color:#14213D
    style F fill:#E0A030,stroke:#B07818,color:#14213D
    style G fill:#12A594,stroke:#0B7C6F,color:#FFFFFF
```

<table>
<tr>
<td width="50%"><img src="https://github.com/ramya-rajendra/p2p-real-data-analysis/raw/main/images/payment_time_distribution.png" alt="Days from vendor invoice to payment" /></td>
<td width="50%"><img src="https://github.com/ramya-rajendra/p2p-real-data-analysis/raw/main/images/issue_impact.png" alt="Extra days caused by payment blocks, changes and cancellations" /></td>
</tr>
</table>

| Finding | |
|---|---|
| Median time from vendor invoice to payment | **64 days** |
| Paid cases with a payment block | **27.6%**, +10 days |
| Extra time when an invoice is cancelled | **+28 days** |
| Share of paid cases from the 10 largest vendors | **31%** |
| Payment block releases done by hand | **73%** |

<details>
<summary><b>What I'd recommend first</b></summary>
<br>

1. Get the payment terms per vendor and check how much early-payment discount is being lost
2. Automate payment block releases when goods receipt and invoice already match, starting with the largest vendors
3. Talk to the three vendors with the highest block rates. One of them alone has over 10,000 cases, a block on more than half, and a median of 112 days to payment
4. Track invoice-to-record time as a KPI, since every day lost there comes out of the payment window

</details>

<br>

## More work

<table>
<tr>
<td width="50%" valign="top">
<img src="https://api.iconify.design/tabler/receipt-euro.svg?color=%23E0A030" height="32" alt="" /><br/>
<b><a href="https://github.com/ramya-rajendra/invoice_automation">Invoice processing</a></b><br/>
<sub>Process analysis and automation prototype that found about €247k a year in lost early-payment discount</sub>
</td>
<td width="50%" valign="top">
<img src="https://api.iconify.design/tabler/book.svg?color=%2312A594" height="32" alt="" /><br/>
<b><a href="https://opus4.kobv.de/opus4-fhws/frontdoor/index/index/docId/6594">Master's thesis</a></b> &nbsp;<sub>(<a href="https://opus4.kobv.de/opus4-fhws/frontdoor/deliver/index/docId/6594/file/Masterarbeit_Rajendra.pdf">PDF</a>)</sub><br/>
<sub>How AI-driven methods could help value a brand when one company buys another</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<img src="https://api.iconify.design/tabler/world-www.svg?color=%231F3A68" height="32" alt="" /><br/>
<b><a href="https://ramya-rajendra.github.io/ramya-portfolio/">Portfolio website</a></b> &nbsp;<sub>(<a href="https://github.com/ramya-rajendra/ramya-portfolio">code</a>)</sub><br/>
<sub>My work in one place, built with HTML and CSS</sub>
</td>
<td width="50%" valign="top">
<img src="https://api.iconify.design/tabler/folders.svg?color=%235B8DEF" height="32" alt="" /><br/>
<b><a href="https://github.com/ramya-rajendra?tab=repositories">All repositories</a></b><br/>
<sub>Every project, including earlier and smaller work</sub>
</td>
</tr>
</table>

<br>

## Background

<table align="center">
<tr>
<td align="center" width="220"><img src="https://api.iconify.design/tabler/device-laptop.svg?color=%233776AB" height="40" alt="" /><br/><b>B.E. Computer Science</b><br/><sub>Visvesvaraya Technological University (VTU), India</sub></td>
<td align="center"><img src="https://api.iconify.design/tabler/arrow-right.svg?color=%238693AD" height="24" alt="then" /></td>
<td align="center" width="220"><img src="https://api.iconify.design/tabler/briefcase.svg?color=%23E0A030" height="40" alt="" /><br/><b>Junior Business Analyst</b><br/><sub>Sri Guru Raghavendra Food Products, India</sub></td>
<td align="center"><img src="https://api.iconify.design/tabler/arrow-right.svg?color=%238693AD" height="24" alt="then" /></td>
<td align="center" width="220"><img src="https://api.iconify.design/tabler/school.svg?color=%2312A594" height="40" alt="" /><br/><b>Master in International Business</b><br/><sub>THWS Würzburg-Schweinfurt, 2025</sub></td>
</tr>
</table>

<p align="center">
  <img src="https://img.shields.io/badge/Hackathon-Prize_winner_at_a_GitHub_hackathon-E0A030?style=flat-square&logo=github&logoColor=white&labelColor=14213D" alt="Prize winner at a GitHub hackathon" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/English-1F3A68?style=flat-square" alt="English" />
  <img src="https://img.shields.io/badge/German-intermediate-1F3A68?style=flat-square&labelColor=1F3A68&color=5B8DEF" alt="German, intermediate" />
  <img src="https://img.shields.io/badge/Kannada-1F3A68?style=flat-square" alt="Kannada" />
  <img src="https://img.shields.io/badge/Telugu-1F3A68?style=flat-square" alt="Telugu" />
</p>

<br>

## Toolbox

<table align="center">
<tr>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" height="40" alt="Python" /><br/><sub>Python</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/pandas/pandas-original.svg" height="40" alt="pandas" /><br/><sub>pandas</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jupyter/jupyter-original.svg" height="40" alt="Jupyter" /><br/><sub>Jupyter</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/matplotlib/matplotlib-original.svg" height="40" alt="matplotlib" /><br/><sub>matplotlib</sub></td>
<td align="center" width="110"><img src="https://cdn.simpleicons.org/googlebigquery/669DF6" height="40" alt="BigQuery" /><br/><sub>BigQuery</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg" height="40" alt="MySQL" /><br/><sub>MySQL</sub></td>
</tr>
<tr>
<td align="center" width="110"><img src="https://cdn.simpleicons.org/duckdb/FFC500" height="40" alt="DuckDB" /><br/><sub>DuckDB</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/sqlite/sqlite-original.svg" height="40" alt="SQLite" /><br/><sub>SQLite</sub></td>
<td align="center" width="110"><img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" height="40" alt="Power BI" /><br/><sub>Power BI</sub></td>
<td align="center" width="110"><img src="https://upload.wikimedia.org/wikipedia/commons/3/31/Microsoft_Office_Excel_%282013%E2%80%932019%29.svg" height="40" alt="Excel" /><br/><sub>Excel</sub></td>
<td align="center" width="110"><img src="https://cdn.simpleicons.org/sap/0FAAFF" height="40" alt="SAP Analytics Cloud" /><br/><sub>SAP Analytics Cloud</sub></td>
<td align="center" width="110"><img src="https://upload.wikimedia.org/wikipedia/commons/b/b4/Celonis_Logo.png" height="40" alt="Celonis" /><br/><sub>Celonis</sub></td>
</tr>
<tr>
<td align="center" width="110"><img src="https://api.iconify.design/tabler/sitemap.svg?color=%23FF6A00" height="40" alt="BPMN" /><br/><sub>BPMN</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jira/jira-original.svg" height="40" alt="Jira" /><br/><sub>Jira</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/confluence/confluence-original.svg" height="40" alt="Confluence" /><br/><sub>Confluence</sub></td>
<td align="center" width="110"><img src="https://upload.wikimedia.org/wikipedia/commons/0/0e/Microsoft_365_%282022%29.svg" height="40" alt="Microsoft 365" /><br/><sub>Microsoft 365</sub></td>
<td align="center" width="110"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" height="40" alt="Git" /><br/><sub>Git</sub></td>
<td align="center" width="110"><img src="https://cdn.simpleicons.org/github/181717/white" height="40" alt="GitHub" /><br/><sub>GitHub</sub></td>
</tr>
</table>

<br>

---

<p align="center">
  <b>Into processes, data and better business decisions? Let's talk.</b><br><br>
  <a href="https://www.linkedin.com/in/ramyarajendra/"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge" alt="Connect on LinkedIn" /></a>
  <a href="mailto:ramyareddy9488@gmail.com"><img src="https://img.shields.io/badge/Email_me-EA4335?logo=gmail&logoColor=white&style=for-the-badge" alt="Email me" /></a>
</p>
