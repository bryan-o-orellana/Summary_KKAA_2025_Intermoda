# Key Accounts Summary: Sell-Out & Inventory 2025

> A **Power BI project** for visualizing **key accounts performance** with a focus on **sell-out data** and **inventory metrics** for 2025.  
> Developed as a **real professional project** for actionable insights in a visually intuitive manner.

>


> ⚠️ **Note:** The full data model and additional measures are **proprietary and confidential**, and are not included in this repository.

## 📝 Project Overview

This repository includes:

- ✅ **Key Inventory Indicators**  
- ✅ **Inventory Cost Summary Cards**  
  ✅ **Theme.json** 
- ✅ **PDF summary report** for easy sharing  

Preview:
>
![PDF Preview](./Performance_KKAA/Preview.png)


## 🛠 Measures (DAX)

---

<details>
  <summary>**1️⃣ Indicador Inventario**</summary>

```DAX
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

➡️ → 0–3 months

⬆️ → 3–5 months

⬇️ → More than 5 months

⚪ → No data available

</details>
<details> <summary>**2️⃣ Inventario Card**</summary>
DAX
Copiar código
Inventario Card = 
VAR Costo = FORMAT(DIVIDE([Costo Total Inventario],1000000),"0.0") & " mill"
VAR Meses = FORMAT([Meses Inventario Promedio],"0.0")
VAR Indicador = [Indicador Inventario]
RETURN
"Costo total: " & Costo & UNICHAR(10) & 
"Meses de inventario: " & Meses & " " & Indicador
Description:
Creates a summary card combining:

Total inventory cost (in millions)

Average months of inventory

Inventory indicator

This measure provides a quick overview of inventory health at a glance.

</details>
📄 PDF Report

Download the full PDF report here:
📥 Download Resumen KKAA 2025

🔗 Connect with Me

🔒 License / Disclaimer
This project is intended for internal professional use.
Full data model, source data, and additional measures are confidential and proprietary to the company.




