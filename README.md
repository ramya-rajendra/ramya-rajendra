<p align="center">
  <img src="assets/header.svg" alt="Ramya Rajendra, business and process analyst" width="100%" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ramyarajendra/">LinkedIn</a>
  &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="mailto:ramyareddy9488@gmail.com">ramyareddy9488@gmail.com</a>
  &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://github.com/ramya-rajendra/ramya-portfolio">Portfolio</a>
</p>

<br>

## What I work on

Most companies already know their processes are slow. What they usually don't know is *where* the time goes and which fix is worth doing first. That's the part I like: taking a process apart step by step, checking it against the data, and turning it into a short list of things someone can actually act on.

I studied Computer Science in India, worked as a marketing analyst, and then did an MBA in International Business at THWS in Würzburg. So I'm comfortable on both sides of the table, with the people running the process and with the data behind it.

<br>

## Featured case: purchase-to-pay on real company data

**[p2p-real-data-analysis](https://github.com/ramya-rajendra/p2p-real-data-analysis)** &nbsp;&nbsp; Python, pandas, SQL (DuckDB)

I took the BPI Challenge 2019 event log, 1.6 million real process steps from the purchase-to-pay process of a large multinational, and asked a simple question: how long does it take to pay a vendor, and what slows it down?

<table>
<tr>
<td width="50%"><img src="https://github.com/ramya-rajendra/p2p-real-data-analysis/raw/main/images/payment_time_distribution.png" alt="Distribution of days from vendor invoice to payment" /></td>
<td width="50%"><img src="https://github.com/ramya-rajendra/p2p-real-data-analysis/raw/main/images/issue_impact.png" alt="Extra days caused by payment blocks, changes and cancellations" /></td>
</tr>
</table>

| Finding | Number |
|---|---|
| Median time from vendor invoice to payment | **64 days** |
| Time before an invoice is even recorded | **10 days** |
| Paid cases that hit a payment block | **27.6%**, adding 10 days |
| Extra time when an invoice is cancelled | **+28 days** |
| Share of paid cases from the 10 largest vendors | **31%** |
| Payment block releases still done by hand | **73%** |

**What I'd do first:** get the payment terms per vendor to see how much early-payment discount is being lost, automate block releases when goods receipt and invoice already match, and talk to the three vendors with the highest block rates. One of them alone has over 10,000 cases, a block on more than half of them, and a median of 112 days to payment.

<br>

## Other work

| Project | The question | How |
|---|---|---|
| **[Invoice automation](https://github.com/ramya-rajendra/invoice_automation)** | Where do manual steps slow down invoice processing, and which ones can follow a simple rule? | Python, synthetic data, routing logic |
| **[MBA thesis](https://opus4.kobv.de/opus4-fhws/frontdoor/deliver/index/docId/6594/file/Masterarbeit_Rajendra.pdf)** | Can AI-driven methods help put a number on a brand when one company buys another? | Master thesis, THWS |
| **[Portfolio site](https://github.com/ramya-rajendra/ramya-portfolio)** | A simple home for my work | HTML, CSS |

<br>

## Background

| | |
|---|---|
| **MBA, International Business** | THWS Würzburg-Schweinfurt, 2025 |
| **B.E., Computer Science** | India |
| **Marketing analyst** | Sri Guru Raghavendra Food Products, India |
| **Hackathon** | Prize winner at a GitHub hackathon |
| **Languages** | Telugu, English, German (intermediate) |

**Tools I use:** Python, pandas, SQL with DuckDB, matplotlib, Git, and HTML/CSS/JavaScript for the odd web page.

<br>

---

I'm looking for business, process and product analyst roles anywhere in Germany. If you have a process everyone complains about but nobody has measured, [I'd like to hear about it](mailto:ramyareddy9488@gmail.com).
