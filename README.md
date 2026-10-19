<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:1C2740,100:2B3A5C&height=170&section=header&text=Ramya%20Rajendra&fontSize=48&fontColor=EEF1F7&fontAlignY=42&desc=Business%20and%20process%20analyst%20%E2%80%94%20finding%20where%20processes%20lose%20time%20and%20money&descSize=17&descAlignY=72&descColor=C9D2E3" width="100%" alt="Ramya Rajendra, business and process analyst" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ramyarajendra/"><img src="https://img.shields.io/badge/LinkedIn-ramyarajendra-1C2740?logo=linkedin&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="LinkedIn" /></a>
  <a href="mailto:ramyareddy9488@gmail.com"><img src="https://img.shields.io/badge/Email-ramyareddy9488%40gmail.com-1C2740?logo=gmail&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="Email" /></a>
  <a href="https://ramya-rajendra.github.io/ramya-portfolio/"><img src="https://img.shields.io/badge/Portfolio-website-1C2740?logo=githubpages&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="Portfolio website" /></a>
  <a href="https://opus4.kobv.de/opus4-fhws/frontdoor/index/index/docId/6594"><img src="https://img.shields.io/badge/MBA_thesis-THWS-1C2740?logo=bookstack&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="MBA thesis" /></a>
</p>

<br>

Most companies already know their processes are slow. What they usually don't know is **where** the time goes and **which fix pays off first**. That's the work I like: mapping a process step by step, checking it against the data, and turning it into a short list of changes with a number attached.

I studied Computer Science in India, worked as a marketing analyst, and then did an MBA in International Business at THWS in Würzburg. So I'm at home on both sides: talking to the people who run a process, and working with the data behind it.

<br>

## Case study 1 &nbsp;·&nbsp; Invoice processing: from process analysis to EBIT impact

**[invoice_automation](https://github.com/ramya-rajendra/invoice_automation)** &nbsp;|&nbsp; Python, pandas, SQL (SQLite), process mapping, Claude API prototype

A mid-sized German manufacturer handles about 12,000 supplier invoices a year, mostly by hand. I mapped the as-is process, analysed a year of invoice data, designed a to-be process and built a small prototype. The company and data are fictional, so the numbers show the method.

<table>
<tr>
<td width="55%"><img src="https://github.com/ramya-rajendra/invoice_automation/raw/main/images/as_is_vs_to_be.png" alt="As-is versus to-be KPIs" /></td>
<td width="45%">

| | As-is | To-be |
|---|---|---|
| Cycle time | 9.0 days | **4.6 days** |
| Discount paid in time | 67% | **95%** |
| Skonto lost / year | €239k | **€51k** |
| Cost per invoice | €15.06 | **€10.12** |

**Estimated EBIT effect: about €247k per year.** Even with conservative assumptions it stays around €186k.

</td>
</tr>
</table>

The surprising part: the biggest cost wasn't clerk time, it was lost early-payment discount. And almost half of it came from invoices that matched perfectly but simply waited, first in the entry backlog and then for the weekly payment run.

<br>

## Case study 2 &nbsp;·&nbsp; Purchase-to-pay on real company data

**[p2p-real-data-analysis](https://github.com/ramya-rajendra/p2p-real-data-analysis)** &nbsp;|&nbsp; Python, pandas, SQL (DuckDB)

To test the same questions on real data, I analysed the BPI Challenge 2019 event log: **1.6 million process steps** from the purchase-to-pay process of a large multinational paint and coatings company.

```mermaid
flowchart LR
    A[Purchase order] --> B[Goods receipt]
    B --> C[Vendor invoice]
    C -- "median 10 days" --> D[Invoice recorded]
    D --> E{Payment block?}
    E -- "27.6% of cases, +10 days" --> F[Manual release]
    E -- "no block" --> G[Paid]
    F --> G
    style C fill:#2B3A5C,stroke:#8693AD,color:#EEF1F7
    style D fill:#2B3A5C,stroke:#8693AD,color:#EEF1F7
    style E fill:#1C2740,stroke:#F2A541,color:#F2A541
    style F fill:#1C2740,stroke:#F2A541,color:#F2A541
    style G fill:#2B3A5C,stroke:#8693AD,color:#EEF1F7
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

## More of my work

| | |
|---|---|
| **[MBA thesis](https://opus4.kobv.de/opus4-fhws/frontdoor/index/index/docId/6594)** &nbsp;([PDF](https://opus4.kobv.de/opus4-fhws/frontdoor/deliver/index/docId/6594/file/Masterarbeit_Rajendra.pdf)) | How AI-driven methods could help value a brand when one company buys another |
| **[Portfolio website](https://ramya-rajendra.github.io/ramya-portfolio/)** &nbsp;([code](https://github.com/ramya-rajendra/ramya-portfolio)) | My work in one place, built with HTML and CSS |

<br>

## Background

| | |
|---|---|
| **MBA, International Business** | THWS Würzburg-Schweinfurt, 2025 |
| **B.E., Computer Science** | India |
| **Marketing analyst** | Sri Guru Raghavendra Food Products, India |
| **Hackathon** | Prize winner at a GitHub hackathon |
| **Languages** | Telugu, English, German (intermediate) |

<p>
  <img src="https://img.shields.io/badge/Python-1C2740?logo=python&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="Python" />
  <img src="https://img.shields.io/badge/pandas-1C2740?logo=pandas&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="pandas" />
  <img src="https://img.shields.io/badge/SQL-1C2740?logo=sqlite&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="SQL" />
  <img src="https://img.shields.io/badge/DuckDB-1C2740?logo=duckdb&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="DuckDB" />
  <img src="https://img.shields.io/badge/matplotlib-1C2740?logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="matplotlib" />
  <img src="https://img.shields.io/badge/Process_mapping-1C2740?logo=mermaid&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="Process mapping" />
  <img src="https://img.shields.io/badge/Git-1C2740?logo=git&logoColor=white&style=for-the-badge&labelColor=1C2740&color=2B3A5C" alt="Git" />
</p>

<br>

---

<p align="center">
  Looking for business, process and product analyst roles anywhere in Germany.<br>
  If you have a process everyone complains about but nobody has measured, <a href="mailto:ramyareddy9488@gmail.com">I'd like to hear about it</a>.
</p>
