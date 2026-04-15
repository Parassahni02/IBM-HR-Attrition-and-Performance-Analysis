# IBM HR Analytics — Key Insights Report
**Dataset:** 1,470 employees | 40 columns | Source: IBM HR Analytics  
**Tools Used:** Excel (Data Cleaning) → PostgreSQL (Analysis) → Power BI (Dashboard)

---

## 📊 Section 1: Attrition Analysis

### Headline Numbers
| Metric | Value |
|--------|-------|
| Total Employees | 1,470 |
| Employees Who Left | 237 |
| Employees Who Stayed | 1,233 |
| **Overall Attrition Rate** | **16.12%** |

---

### Attrition by Department
| Department | Total | Left | Attrition Rate |
|------------|-------|------|----------------|
| Sales | 446 | 92 | **20.63%** |
| Human Resources | 63 | 12 | 19.05% |
| Research & Development | 961 | 133 | 13.84% |

**Finding:** Sales has the highest attrition rate at 20.63% — nearly 1 in 5 Sales employees leave. Despite being the largest department, R&D has the lowest rate.

---

### Attrition by Job Role
| Job Role | Total | Left | Attrition Rate | Avg Income |
|----------|-------|------|----------------|------------|
| Sales Representative | 83 | 33 | **39.76%** | $2,626 |
| Laboratory Technician | 259 | 62 | 23.94% | $3,237 |
| Human Resources | 52 | 12 | 23.08% | $4,236 |
| Sales Executive | 326 | 57 | 17.48% | $6,924 |
| Research Scientist | 292 | 47 | 16.10% | $3,240 |
| Manufacturing Director | 145 | 10 | 6.90% | $7,295 |
| Healthcare Representative | 131 | 9 | 6.87% | $7,529 |
| Manager | 102 | 5 | 4.90% | $17,182 |
| Research Director | 80 | 2 | **2.50%** | $16,034 |

**Finding:** Sales Representatives have a shocking **39.76% attrition rate** — nearly 4 in 10 leave. Research Directors are the most stable at only 2.50%. The pattern is clear: lower income roles lose people faster.

---

### Attrition by Age Group
| Age Group | Total | Left | Attrition Rate | Avg Income | Avg Tenure |
|-----------|-------|------|----------------|------------|------------|
| 18–25 | 123 | 44 | **35.77%** | $2,973 | 2.5 yrs |
| 26–35 | 606 | 116 | 19.14% | $4,896 | 6.0 yrs |
| 46–60 | 273 | 34 | 12.45% | $10,630 | 9.4 yrs |
| 36–45 | 468 | 43 | **9.19%** | $7,104 | 8.1 yrs |

**Finding:** Young employees (18–25) leave at a rate of **35.77%** — over 2x the company average. This is early-career churn: low pay, limited growth visibility, and high job-hopping tendency. The 36–45 group is the most stable.

---

### Overtime Impact on Attrition
| Overtime | Total | Left | Attrition Rate |
|----------|-------|------|----------------|
| Yes | 416 | 127 | **30.53%** |
| No | 1,054 | 110 | 10.44% |

**Finding:** Employees working overtime leave at **3x the rate** of those who don't. This is one of the strongest single-factor drivers of attrition in the dataset.

---

### Attrition by Marital Status
| Marital Status | Total | Left | Attrition Rate |
|----------------|-------|------|----------------|
| Single | 470 | 120 | **25.53%** |
| Married | 673 | 84 | 12.48% |
| Divorced | 327 | 33 | 10.09% |

**Finding:** Single employees leave at **2.5x the rate** of divorced employees. Single employees have less financial obligation, making job switching easier.

---

### Attrition by Business Travel
| Travel Frequency | Total | Left | Attrition Rate |
|------------------|-------|------|----------------|
| Travel Frequently | 277 | 69 | **24.91%** |
| Travel Rarely | 1,043 | 156 | 14.96% |
| Non-Travel | 150 | 12 | 8.00% |

**Finding:** Frequent travelers leave at **3x the rate** of non-travelers, strongly suggesting travel fatigue is a hidden attrition driver.

---

### Attrition by Gender
| Gender | Total | Left | Attrition Rate |
|--------|-------|------|----------------|
| Male | 882 | 150 | **17.01%** |
| Female | 588 | 87 | 14.80% |

**Finding:** Male attrition is slightly higher, but the gap is small (~2%). Gender alone is not a significant predictor — other factors are far more influential.

---

### Attrition by Tenure Band
| Tenure Band | Total | Left | Attrition Rate |
|-------------|-------|------|----------------|
| 0–2 yrs | 424 | 83 | **19.58%** |
| 3–5 yrs | 556 | 108 | **19.42%** |
| 6–10 yrs | 312 | 33 | 10.58% |
| 10+ yrs | 178 | 13 | 7.30% |

**Finding:** The first 5 years are the danger zone — employees with less than 5 years tenure account for the vast majority of attrition. Those who survive past 6 years are significantly more likely to stay long-term.

---

## 🚨 Section 2: High Risk Analysis

### The Typical Employee Who Left vs Stayed
| Metric | Stayed (No) | Left (Yes) | Difference |
|--------|-------------|------------|------------|
| Average Age | 37.6 yrs | **33.6 yrs** | -4 years younger |
| Avg Monthly Income | $6,833 | **$4,787** | -$2,046 less |
| Avg Tenure | 7.4 yrs | **5.1 yrs** | -2.3 years less |
| Avg Job Satisfaction | 2.78 | **2.47** | Lower |
| Avg Work-Life Balance | 2.78 | **2.66** | Lower |
| Avg Environment Satisfaction | 2.77 | **2.46** | Lower |
| Avg Distance From Home | 8.9 km | **10.6 km** | Further away |
| Avg Prev Companies Worked | 2.65 | **2.94** | More job-hoppers |

**Finding:** A typical employee who left was younger, earned significantly less, had lower scores across all 3 satisfaction dimensions, lived further from work, and had worked at more companies — a classic profile of disengaged, underpaid early-career talent.

---

### The Triple Risk Combo
**Overtime = Yes + Single + Age 18–25**

| Metric | Value |
|--------|-------|
| Employees in this group | 21 |
| Employees who left | 16 |
| **Attrition Rate** | **76.2%** |
| Company Average | 16.12% |

**Finding:** This combination is the single most dangerous risk profile in the dataset — **76% attrition rate**, nearly 5x the company average. Young, single, overworked employees are almost certain to leave.

---

### Overtime × Job Satisfaction Heatmap
| Overtime | Job Satisfaction | Attrition Rate |
|----------|-----------------|----------------|
| Yes | Medium | **37.68%** |
| Yes | Low | **35.71%** |
| Yes | High | **33.88%** |
| Yes | Very High | 21.13% |
| No | Low | 17.56% |
| No | High | 9.97% |
| No | Medium | 9.48% |
| No | Very High | **6.94%** |

**Finding:** Even employees with **Very High job satisfaction** leave at 21% when they work overtime. Overtime overrides satisfaction — it's not enough to make people happy if they're being overworked.

---

### Job Level 1 — The Attrition Hotspot
Job Level 1 has a **26.34% attrition rate** — the highest of all levels.

| Job Role (Level 1) | Total | Left | Attrition Rate |
|--------------------|-------|------|----------------|
| Sales Representative | 76 | 32 | **42.11%** |
| Human Resources | 33 | 10 | 30.30% |
| Laboratory Technician | 200 | 56 | **28.00%** |
| Research Scientist | 234 | 45 | 19.23% |

**Finding:** Entry-level Sales Representatives have a **42% attrition rate**. These roles typically have the lowest pay, highest pressure, and least recognition — a perfect attrition storm.

---

### Attrition by Job Level
| Job Level | Count | Avg Income | Left | Attrition Rate |
|-----------|-------|------------|------|----------------|
| 1 | 543 | $2,787 | 143 | **26.34%** |
| 2 | 534 | $5,502 | 52 | 9.74% |
| 3 | 218 | $9,817 | 32 | 14.68% |
| 4 | 106 | $15,504 | 5 | 4.72% |
| 5 | 69 | $19,192 | 5 | 7.25% |

**Finding:** Level 1 ($2,787 avg) has a **26.34% attrition rate** vs Level 4 ($15,504 avg) at just 4.72%. Income level is the single strongest predictor of whether someone stays.

---

## 💰 Section 3: Salary Analysis

### Monthly Income by Department
| Department | Avg Income | Median Income | Min | Max |
|------------|------------|---------------|-----|-----|
| Sales | $6,959 | $5,754 | $1,052 | $19,847 |
| Human Resources | $6,655 | $3,886 | $1,555 | $19,717 |
| R&D | $6,281 | $4,374 | $1,009 | $19,999 |

**Finding:** All three departments have very similar average salaries (~$6,300–$6,900), but R&D has the lowest and Sales has the highest — yet Sales also has the highest attrition. This suggests role-level income disparity within Sales is the real problem, not department-level averages.

---

### Monthly Income by Job Role
| Job Role | Avg Income | Median | Min | Max |
|----------|------------|--------|-----|-----|
| Manager | $17,182 | $17,454 | $11,244 | $19,999 |
| Research Director | $16,034 | $16,510 | $11,031 | $19,973 |
| Healthcare Representative | $7,529 | $6,811 | $4,000 | $13,966 |
| Manufacturing Director | $7,295 | $6,447 | $4,011 | $13,973 |
| Sales Executive | $6,924 | $6,231 | $4,001 | $13,872 |
| Human Resources | $4,236 | $3,093 | $1,555 | $10,725 |
| Research Scientist | $3,240 | $2,888 | $1,009 | $9,724 |
| Laboratory Technician | $3,237 | $2,886 | $1,102 | $7,403 |
| Sales Representative | $2,626 | $2,579 | $1,052 | $6,632 |

**Finding:** Managers earn **6.5x more** than Sales Representatives. The income gap between top and bottom roles is enormous — and the lowest earners show the highest attrition. Sales Representatives' max salary ($6,632) is still below the average income of Healthcare Representatives.

---

### Performance vs Salary Hike
| Performance Rating | Label | Avg Hike | Avg Income | Attrition |
|--------------------|-------|----------|------------|-----------|
| 4 | Outstanding | **21.85%** | $6,314 | 16.37% |
| 3 | Excellent | 14.00% | $6,537 | 16.08% |

**Finding:** Outstanding performers get a bigger hike (21.85% vs 14%), but their **average income is actually lower** than Excellent performers ($6,314 vs $6,537). This suggests outstanding performers tend to be in lower-paid roles, and even a large % hike may not be enough to retain them.

---

### Salary by Education Level
| Education | Avg Income | Median |
|-----------|------------|--------|
| Doctor | $8,278 | $6,203 |
| Master | $6,832 | $5,342 |
| Bachelor | $6,517 | $4,762 |
| College | $6,227 | $4,892 |
| Below College | $5,641 | $3,849 |

**Finding:** Doctors earn 47% more on average than Below College employees. Education has a clear positive income gradient, though the gap narrows significantly above Bachelor level.

---

### Salary by Gender
| Gender | Avg Income | Median |
|--------|------------|--------|
| Female | $6,687 | $5,082 |
| Male | $6,381 | $4,838 |

**Finding:** Females actually earn slightly more on average (+$306) than males. No significant gender pay gap exists in this dataset.

---

## 🔑 Top 5 Actionable Recommendations

1. **Fix Sales Representative compensation immediately** — 39.76% attrition on a role this common is unsustainable. Their max salary ($6,632) should be the floor, not the ceiling.

2. **Create an overtime policy** — Overtime employees leave at 30.53% vs 10.44%. Capping or compensating overtime could cut overall attrition significantly.

3. **Build an early-tenure retention program (Years 0–5)** — 19.5% attrition in the first 5 years. Structured onboarding, mentorship, and a clear promotion roadmap for this group would directly reduce churn.

4. **Flag the triple-risk profile** — Single + Overtime + 18–25 = 76.2% attrition. HR should proactively engage this segment with flexible work, growth conversations, and career pathing.

5. **Promote faster at Job Level 1** — 26.34% attrition at the entry level. Employees stuck at Level 1 with no visible path upward will leave. A structured 18-month promotion target for high-performing Level 1 employees would help retain them.


*Analysis performed using PostgreSQL | Dashboard built in Power BI*
