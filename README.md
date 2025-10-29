
## 🧠 Key Accounts Summary: Sell-Out & Inventory 2025 for Intermoda S.A.

> A **Power BI project** for visualizing **key accounts performance** with a focus on **sell-out data** and **inventory metrics** for 2025.  
> Developed as a **real professional project FOR Intermoda S.A.** for actionable insights in a visually intuitive manner.

---

## 🗂️ Project Overview
This project presents a detailed overview of **Key Account (KKAA) clients**, highlighting:
- **Sell-out sales summary**
- **Inventory summary**

---
## 🗂️ Project Structure

The repository is organized as follows:

/Performance_KKAA
- ✅ **Preview.png**  
- ✅ **Reference.png**  
- ✅ **Theme.json**
- ✅ **jpg image reference** 
- ✅ **Resumen_KKAA (PDF summary report)** for easy sharing

Each file provides specific documentation or visual reference for the **Summary_KKAA_2025_Intermoda** Business Intelligence project.

---
## 📊 Preview
>
>![PDF Preview](./Performance_KKAA/Preview.png)

---
## 🧮 Main DAX Measures
- `Indicador Inventario`  
- `Inventario Card`
>
**# 1. `Indicador Inventario`**

Indicador Inventario = 
VAR Meses = [Meses Inventario Promedio]
RETURN
SWITCH(
    TRUE(),
    Meses >= 0 && Meses < 3, " ➡️",
    Meses >= 3 && Meses <= 5, " ⬆️",
    Meses > 5, " ⬇️",
    "⚪"  -- If no data
)
Description:
Assigns an inventory indicator icon based on the average months of inventory:

➡️ for 0–3 months

⬆️ for 3–5 months

⬇️ for more than 5 months

⚪ if there is no data

**# 2.`Inventario Card`**

Inventario Card = 
VAR Costo = FORMAT(DIVIDE([Costo Total Inventario],1000000),"0.0") & " mill"
VAR Meses = FORMAT([Meses Inventario Promedio],"0.0")
VAR Indicador = [Indicador Inventario]
RETURN
"Costo total: " & Costo & UNICHAR(10) & 
"Meses de inventario: " & Meses & " " & Indicador

---

## 🧰 Tools & Technologies
| Tool | Purpose |
|------|----------|
| **Power BI Desktop (Sept 2025)** | Report creation |
| **DAX Studio** | Measure validation |
| **SQL Server** | Data source |
| **GitHub** | Version control |

---

## 🗃️ Data Sources
- Internal **OLAP Cubes**
- Extracted and modeled in **Power Query**


## 📄 Report File
[📥 Download Report (PDF)](./Summary_KKAA_2025_Intermoda/Resumen_KKAA.pdf)

## 💬 Author
**Bryan Odair Orellana Chávez**  
Business Intelligence & Data Analysis  

![🔗 Contact me on LinkedIn](https://www.linkedin.com/in/bryanxavez)

## 📄 Design reference
[📥 Image of reference)](./Summary_KKAA_2025_Intermoda/Reference.pdf)
---
License / Disclaimer

This project is intended for internal professional use. Data and full model structures are confidential and proprietary to the company Intermoda .S.A.
---
## 🏷️ Tags
`#PowerBI` `#DAX` `#BusinessIntelligence` `#DataAnalytics` `#SQLServer`

