# 🥤 Product Positioning through Pricing: Kiwi Bubbles  

What happens when a strong brand faces a bubbly competitor?  
This project tells the story of **Kiwi**, a leading soft drink company, deciding whether to launch its new product **Kiwi Bubbles (KB)** to compete with **Mango Bubbles (MB)**.  

Using **choice data from 359 consumers over 3 years**, we applied econometric modeling, market segmentation, and strategic simulations to determine **if Kiwi Bubbles should launch, how to price it, and how to position it against Mango**.  

---

## 📖 The Business Question  

- Kiwi Regular (KR) is doing well in the market.  
- Mango Bubbles (MB) is winning consumers who prefer carbonation.  
- Kiwi wonders: *If we launch Kiwi Bubbles (KB), will it expand our profit or just cannibalize KR? And how will Mango react?*  

---

## 🔬 Analytical Approach  

### 1. **Baseline Demand Estimation** (No Segmentation)  
We started with a **multinomial logit model** using consumer purchase data.  

**Model results:**  
- Price coefficient: **-3.74** (p < 0.001) → demand is strongly price-sensitive.  
- Intercepts:  
  - KR: **4.36** → most preferred baseline.  
  - KB: **4.25** → nearly as strong as KR.  
  - MB: **4.20** → slightly weaker preference than Kiwi products.  

**Elasticities at average prices:**  
- Own-price elasticities:  
  - KB = **4.26**  
  - KR = **4.13**  
  - MB = **4.07**  
- Cross-price elasticities were all **≤ 1**, meaning weak substitution across products.  

**Optimal price (no segmentation):**  
- KB = **$1.16**, profit ≈ **$186**  
- KR = **$1.16**, profit ≈ **$207**  
- MB = profit ≈ **$91**  

📌 *Insight:* Demand is elastic, but surprisingly, substitution appeared weaker than expected given similar prices.  

---

### 2. **Segmentation with K-Means**  
Not all shoppers behave alike — so we clustered consumers into **9 segments** using demographics, then re-estimated demand.  

**Findings:**  
- **Segments 2, 6, 9** showed stronger preference for Kiwi Bubbles over Kiwi Regular.  
- **Segments 4, 5, 7, 8** leaned toward Kiwi Regular.  
- MB dominated in segments 1, 2, and 6.  
- **Most price-sensitive clusters:** Segments 2 & 6 (price coefficient ≈ -5.9).  
- **Least price-sensitive cluster:** Segment 4 (price coefficient ≈ -1.25).  

**Elasticities with segmentation:**  
- Own-price elasticities:  
  - KB = **4.38**  
  - KR = **3.63**  
  - MB = **4.28**  
- Cross-price elasticities:  
  - KB ↔ MB: **1.08** → now clear substitutes.  
  - KR ↔ KB: **0.81** → weaker cannibalization.  

📌 *Insight:* Segmentation revealed that Kiwi Regular became more differentiated, while KB and MB turned into stronger substitutes — a realistic reflection of market behavior.  

---

### 3. **Profit Optimization**  

- Without KB:  
  - Optimal KR price = **$1.06**, profit ≈ **$297**.  

- With KB launched:  
  - Optimal KB = **$1.60**, Optimal KR = **$1.60**.  
  - Kiwi’s total profit increased by ≈ **$251**.  
  - MB profit rose to ≈ **$361** (indicating KB’s launch also lifted MB, perhaps due to consumer preference overlap).  

📌 *Insight:* Launching KB raises Kiwi’s profit, but also indirectly benefits Mango — suggesting Kiwi must carefully manage positioning to capture bubble-preferring segments (2 & 9).  

---

### 4. **Competitive Simulation (Pricing War)**  
Finally, we simulated a **pricing war** where Kiwi and Mango iteratively adjust prices until equilibrium.  

- Mango’s best response to Kiwi’s initial prices: drop MB to **$1.00**.  
- Kiwi’s response: KB = **$1.04**, KR = **$1.08**.  
- Profits stabilized with Kiwi maintaining advantage, but Mango staying competitive through aggressive pricing.  

📌 *Insight:* Kiwi Bubbles is sustainable even in a competitive environment — but success requires anticipating Mango’s countermoves.  

---

## 📊 Key Takeaways  

- **Kiwi Bubbles can succeed**: demand exists, especially among bubble-loving, price-sensitive segments.  
- **Cannibalization is limited**: segmentation shows KR maintains loyal buyers.  
- **Mango remains a threat**: KB and MB are close substitutes, so competitive pricing matters.  
- **Strategic positioning**: focus KB on Segments 2 & 9 (loyal bubble fans) while keeping KR premium and differentiated.  

---

## 🛠️ Tools & Methods  

- **R**: `mlogit`, `gmnl`, `data.table`, clustering methods  
- **Models**: Multinomial logit, segmented logit, elasticity analysis  
- **Analysis**: Demand estimation, profit optimization, competitive equilibrium simulation  
- **Data**:  
  - `kiwi_bubbles.csv` & variants – purchase data  
  - `demo_description.xlsx` – consumer demographics  

---

## 🌟 Why This Project Matters  

This case illustrates the **end-to-end logic of pricing analytics**:  
1. Estimate demand.  
2. Recognize consumer heterogeneity.  
3. Optimize pricing under different scenarios.  
4. Anticipate competitor response.  

The story of Kiwi Bubbles shows how analytics translates raw consumer data into **actionable pricing and positioning strategy** — insights every company needs in competitive markets.  
