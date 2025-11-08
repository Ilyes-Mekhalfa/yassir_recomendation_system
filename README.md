<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/4/49/Yassir_logo.png" alt="Yassir Logo" width="180"/>
</p>

<h1 align="center">🧠 Yassir AI Market Challenge — Team Recommender System</h1>

<p align="center">
  <b>Hackathon Project Submission</b><br/>
  <i>Developed by Team Participants of the Yassir AI Hackathon</i>
</p>

---

## 📖 Overview

This repository contains our **team’s final submission code** for the **Yassir AI Market Challenge Hackathon**.  
The project implements a **simple, rule-based recommender system** that achieved a **score of 0.21998** on the public leaderboard.  

The goal was to predict the top 10 products each user is most likely to purchase next, based on their past orders and category preferences.

---

## 🧩 Key Features

- 📦 **Order-based recommendations** — Uses user purchase frequency.  
- 🏷️ **Category-aware suggestions** — Incorporates user favorite product categories.  
- 🔥 **Global popularity fallback** — Handles cold-start users gracefully.  
- ⚡ **Chunked CSV processing** — Efficiently handles large datasets.  
- 🧠 **Simple yet effective** — No ML model, just smart heuristics.  

---

## 🧠 Recommendation Logic

The recommender follows **three main steps**:

| Step | Description | Data Source |
|------|--------------|-------------|
| 1️⃣ | Recommend the user’s most frequently purchased products | User order history |
| 2️⃣ | Add popular products from their favorite categories | Category data |
| 3️⃣ | Fill remaining slots with overall popular products | Global order data |

This hybrid strategy ensures both personalization and generalization.

---

## 🗂️ Project Structure

```
├── main.ipynb                       # Main code file (this repository)
├── submission.csv     # Generated submission file
├── /data                         # Dataset directory (Kaggle inputs)
│   ├── products.csv
│   ├── orders_df.csv
│   ├── orders_products_df.csv
│   ├── category_df.csv
|   ├── sub_category_df.csv
|   ├── user_test_df.csv
|   ├── users_df.csv
└── README.md                     # This documentation
```

---

## ⚙️ Requirements

Install dependencies using:

```bash
pip install pandas numpy
```

**Python version:** 3.8 or later

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Ilyes-Mekhalfa/yassir_recomendation_system.git
   cd yassir_recomendation_system
   ```

2. Place the Kaggle dataset files in the `/data/` folder, or update paths inside `main.py`.

3. Run the main script:
   ```bash
   python main.py
   ```

4. The script will output:
   ```
   exact_original_021998.csv
   ```
   This file contains the final 10 recommendations per user for submission.

---

## 📊 Output Format

| user_id | product_id                     |
|----------|--------------------------------|
| 1001     | 233 54 88 109 210 322 444 ... |
| 1002     | 56 22 91 305 78 129 443 ...   |

Each row represents one user with their top 10 predicted product IDs, space-separated.

---

## 🏆 Hackathon Context

This code was created as part of the **Yassir AI Hackathon Challenge 2025**,  
where participants developed algorithms to predict user purchasing behavior using Yassir Market data.

- **Competition Organizer:** [Yassir](https://yassir.com)
- **Challenge Type:** AI Recommender System
- **Score Achieved:** 0.21998 (Public Leaderboard)
- **Approach:** Rule-based heuristic recommender

---

## 🧑‍💻 Team Members

| Name | Role | Focus |
|------|------|--------|
| **Khatir Redha** | Data & Code Integration | Data processing, feature engineering |
| **Ilyes Mekhalfa** | ML Engineer | Recommendation logic, optimization |
| **Boualdja Aymen** | Data Analyst | Dataset cleaning, analysis |
| **Allouch Moaad** | Full-Stack Developer | Integration & testing |

---

## 🪪 License

This project is released under the **MIT License** — free to use, modify, and distribute with attribution.

---

<p align="center">
  Made with ❤️ for the <b>Yassir AI Market Hackathon</b><br/>
  <i>Empowering intelligent commerce through data.</i>
</p>
