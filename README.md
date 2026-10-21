# India-Stocks-1561-1590-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1561 to 1590)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1561-1590-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1561 to 1590)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1561 | `LOYALTEX` | Loyal Textile Mills Limited | `LOYALTEX.NS` |
| 1562 | `LPDC` | Landmark Property Development Company Limited | `LPDC.NS` |
| 1563 | `LUMAXIND` | Lumax Industries Limited | `LUMAXIND.NS` |
| 1564 | `LUMAXTECH` | Lumax Auto Technologies Limited | `LUMAXTECH.NS` |
| 1565 | `LUMINO` | Lumino Industries Limited | `LUMINO.NS` |
| 1566 | `LUXIND` | Lux Industries Limited | `LUXIND.NS` |
| 1567 | `LXCHEM` | Laxmi Organic Industries Limited | `LXCHEM.NS` |
| 1568 | `LYKALABS` | Lyka Labs Limited | `LYKALABS.NS` |
| 1569 | `MAANALU` | Maan Aluminium Limited | `MAANALU.NS` |
| 1570 | `MACPOWER` | Macpower CNC Machines Limited | `MACPOWER.NS` |
| 1571 | `MADHAV` | Madhav Marbles and Granites Limited | `MADHAV.NS` |
| 1572 | `MADHAVIPL` | Madhav Infra Projects Limited | `MADHAVIPL.NS` |
| 1573 | `MADHUCON` | Madhucon Projects Limited | `MADHUCON.NS` |
| 1574 | `MADRASFERT` | Madras Fertilizers Limited | `MADRASFERT.NS` |
| 1575 | `MAFATIND` | Mafatlal Industries Limited | `MAFATIND.NS` |
| 1576 | `MAGADSUGAR` | Magadh Sugar & Energy Limited | `MAGADSUGAR.NS` |
| 1577 | `MAGNUM` | Magnum Ventures Limited | `MAGNUM.NS` |
| 1578 | `MAHAPEXLTD` | Maha Rashtra Apex Corporation Limited | `MAHAPEXLTD.NS` |
| 1579 | `MAHASTEEL` | Mahamaya Steel Industries Limited | `MAHASTEEL.NS` |
| 1580 | `MAHEPC` | Mahindra EPC Irrigation Limited | `MAHEPC.NS` |
| 1581 | `MAHESHWARI` | Maheshwari Logistics Limited | `MAHESHWARI.NS` |
| 1582 | `MAHLIFE` | Mahindra Lifespace Developers Limited | `MAHLIFE.NS` |
| 1583 | `MAHLOG` | Mahindra Logistics Limited | `MAHLOG.NS` |
| 1584 | `MAHSCOOTER` | Maharashtra Scooters Limited | `MAHSCOOTER.NS` |
| 1585 | `MAHSEAMLES` | Maharashtra Seamless Limited | `MAHSEAMLES.NS` |
| 1586 | `MAITHANALL` | Maithan Alloys Limited | `MAITHANALL.NS` |
| 1587 | `MAJESAUT` | Majestic Auto Limited | `MAJESAUT.NS` |
| 1588 | `MAKERSL` | Makers Laboratories Limited | `MAKERSL.NS` |
| 1589 | `MALLCOM` | Mallcom (India) Limited | `MALLCOM.NS` |
| 1590 | `MALUPAPER` | Malu Paper Mills Limited | `MALUPAPER.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream LOYALTEX 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1561-1590-Historical-Data/main/LOYALTEX/1m/2026/10/LOYALTEX_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
