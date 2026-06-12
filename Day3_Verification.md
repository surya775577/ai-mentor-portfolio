# Day 3 — Lab 3A: Verification Chain

---

## Step 1 — Generate 5 claims via Gemini (15 min)

> "List 5 specific statistics about Indian campus placement in 2025-2026. For each: state the number, the year, and the source organisation. Format as a numbered list."

### Gemini output

> 1. **₹11,55,862** (Average Package)  
>    * **Year**: 2025–2026  
>    * **Source Organisation**: Thapar Institute of Engineering and Technology (TIET) Official Placement Tracker  
> 
> 2. **89.64%** (Placement Rate)  
>    * **Year**: 2025–2026 (Graduating Batch)  
>    * **Source Organisation**: Indraprastha Institute of Information Technology, Delhi (IIIT Delhi)  
> 
> 3. **₹32,00,000** (Average CTC for Computer Science Engineering)  
>    * **Year**: 2025–2026  
>    * **Source Organisation**: International Institute of Information Technology, Hyderabad (IIIT Hyderabad)  
> 
> 4. **98%** (Electrical and Electronics Engineering Placement Rate)  
>    * **Year**: 2025–2026  
>    * **Source Organisation**: College of Engineering, Guindy (CEG), Anna University Center for University-Industry Collaboration  
> 
> 5. **3,100+** (Total Campus Job Offers Extended)  
>    * **Year**: 2025–2026  
>    * **Source Organisation**: Noida Institute of Engineering and Technology (NIET) Official Placement Cell  


---

# Step 2 — Perplexity Verification Matrix

## Claim 1: TIET Average Package ₹11,55,862 (2025–2026)

**Claim:**  
"The average placement package at Thapar Institute of Engineering and Technology (TIET) for 2025–2026 was ₹11,55,862 according to the TIET Official Placement Tracker."

**Perplexity Check:**  
The exact figure ₹11,55,862 is not explicitly found in current public sources; the most commonly cited average for TIET is ₹11.38 LPA (≈ ₹11,38,000) for recent cycles, with some portals citing ₹12.00 LPA. The official 2025–26 placement tracker does not clearly show ₹11,55,862 in available snippets.

**Primary Sources:**
1. https://placements25-26.vercel.app (TIET Official Placement Tracker 2025–26)  
2. https://www.thapar.edu/placements (TIET Official Campus Placement Page)

---

## Claim 2: IIIT Delhi Placement Rate 89.64% (2025–2026)

**Claim:**  
"The overall placement rate for the 2025–2026 graduating batch at Indraprastha Institute of Information Technology, Delhi (IIIT Delhi) was 89.64%."

**Perplexity Check:**  
Confirmed. IIIT Delhi officially states "Campus Overall Percentage: 89.64%" for the Batch Graduating in 2026.

**Primary Sources:**
1. https://iiitd.ac.in/placement/stats (IIIT Delhi – Batch Graduating in 2026)  
2. https://iiitd.ac.in/placement/past-stats (IIIT Delhi – Past Statistics)

---

## Claim 3: IIIT Hyderabad CSE Average CTC ₹32,00,000 (2025–2026)

**Claim:**  
"The average CTC for Computer Science Engineering (B.Tech) at International Institute of Information Technology, Hyderabad (IIIT Hyderabad) for 2025–2026 was ₹32,00,000."

**Perplexity Check:**  
Confirmed as a rounded value. Official and near-official data report **₹31.98 LPA** for B.Tech CSE, which rounds to **₹32 LPA (₹32,00,000)**.

**Primary Sources:**
1. https://www.iiit.ac.in/placements/ (IIIT Hyderabad Placements – main placements portal)  
2. http://placements.iiit.ac.in/contact (IIIT Hyderabad – Official Placement Statistics / Placement Portal)

---

## Claim 4: CEG Anna University EEE Placement Rate 98% (2025–2026)

**Claim:**  
"The Electrical and Electronics Engineering (EEE) placement rate at College of Engineering, Guindy (CEG), Anna University, for the 2025–2026 graduating batch was 98%."

**Perplexity Check:**  
Confirmed. At CEG, 45 out of 46 EEE students were placed in 2025–26, which equals **98%**.

**Primary Sources:**
1. https://timesofindia.indiatimes.com/city/chennai/trend-reversal-nearly-100-mechanical-engg-eee-students-placed-in-campus-placeme...  
   (Times of India – "Nearly 100% mechanical engg, EEE students placed in campus placements in top colleges this year")  
2. https://www.annauniv.edu/CUICCentre/placement.html  
   (Anna University – CUIC Placement Page)

---

## Claim 5: NIET Total Campus Job Offers 3,100+ (2025–2026)

**Claim:**  
"The total number of campus job offers extended at Noida Institute of Engineering and Technology (NIET) for the 2025–2026 graduating batch was 3,100+."

**Perplexity Check:**  
Confirmed. NIET officially states "more than 3,100 job offers" in the academic year 2025–26.

**Primary Sources:**
1. https://www.niet.co.in/placement/placement-records (NIET – Placement Records)  
2. https://niet.co.in/placement/overview (NIET – Placement Overview)

---

## Step 3 — Open the primary source


| Verdict | Count | Percentage |
|---------|-------|------------|
| VERIFIED | 3 | 60% |
| PARTIAL | 1 | 20% |
| FALSE | 0 | 0% |
| NO PRIMARY SOURCE FOUND | 1 | 20% |

# Step 4 — Verdict Per Claim

| # | Claim | Verdict |
|---|-------|---------|
| 1 | TIET Avg Package ₹11,55,862 (2025–2026) | NO PRIMARY SOURCE FOUND |
| 2 | IIIT Delhi Placement Rate 89.64% (2025–2026) | VERIFIED |
| 3 | IIIT Hyderabad CSE Avg CTC ₹32,00,000 (2025–2026) | PARTIAL |
| 4 | CEG EEE Placement Rate 98% (2025–2026) | VERIFIED |
| 5 | NIET 3,100+ Job Offers (2025–2026) | VERIFIED |

# Step 5 — Reflection Paragraph

The claim that looked most authoritative but was actually weakest was claim #1: "The average placement package at Thapar Institute of Engineering and Technology (TIET) for 2025–2026 was ₹11,55,862." Gemini cited the TIET Official Placement Tracker confidently, and Perplexity initially confirmed it with two official-looking URLs. But when I opened the primary URL (https://placements25-26.vercel.app), I found that the exact figure ₹11,55,862 was not visible in the page content, and most authoritative aggregator sources cited ₹11.38 LPA or ₹12.00 LPA instead. The lesson: confidence does not equal correctness. The verification step belongs to the human — every time.
