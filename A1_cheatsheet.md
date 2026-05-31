Slide 24 stops right at the end of Exercise 1 (the CDF/PDF solve-for-constant exercise), so the quiz covers **probability rules + random variables + CDF/PMF/PDF only** — joint distributions, independence, and conditional distributions from Topic 2 are **NOT included**.  Here's the fully updated cheat sheet: [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

# 📊 STAT 271 — Quiz 1 Master Cheat Sheet
## Topic 1 (Full) + Topic 2 Slides 1–24

***

## PART 1 — DESCRIPTIVE STATISTICS (Topic 1, Ross Ch. 1–2)

***

## 🔑 Core Concepts

| Term | Plain English |
|---|---|
| **Descriptive stats** | Describe/summarize data — tables, graphs, numbers |
| **Inferential stats** | Draw conclusions about a **population** from a **sample** |
| **Population** | The entire group you want to study |
| **Sample** | A subgroup you actually measure |
| **Representative sample** | Must be chosen **at random** — size alone ≠ representative |
| **Bias** | Systematic distortion favoring certain values |
| **Observational study** | No intervention — e.g., surveys → shows **association** only |
| **Experiment** | Researcher imposes a treatment → can show **causation** |
| **Independent variable** | What you manipulate (the "cause") |
| **Dependent variable** | What you measure (the "effect") |

> ⚠️ Only a **randomized controlled experiment** can establish causation. Observational studies cannot. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/be335a48-1a37-4d84-8d8e-7fa9f1b9082a/Topic-1-Descriptive-statistics-Annotated-May-21.pdf)

***

## 📐 Central Tendency

**Sample Mean:**
\[\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i\]

With frequency table (\(k\) distinct values \(v_i\), frequencies \(f_i\), \(n = \sum f_i\)):
\[\bar{x} = \frac{\sum_{i=1}^{k} f_i v_i}{n}\]

**Sample Median** (sort data first, label \(x_{(1)} \leq x_{(2)} \leq \cdots \leq x_{(n)}\)):
\[m = \begin{cases} x_{((n+1)/2)} & n \text{ odd} \\ \dfrac{x_{(n/2)} + x_{(n/2+1)}}{2} & n \text{ even} \end{cases}\]

**Sample Mode:** Most frequent value(s).

**Key property of the mean:**
\[\sum_{i=1}^{n}(x_i - \bar{x}) = 0 \quad \text{(deviations always sum to zero)}\]

> 💡 Mean is affected by outliers. Median is not. Skewed data → prefer median. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/be335a48-1a37-4d84-8d8e-7fa9f1b9082a/Topic-1-Descriptive-statistics-Annotated-May-21.pdf)

***

## 📐 Dispersion (Spread)

**Sample Variance:**
\[s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2\]

**Shortcut (faster by hand):**
\[s^2 = \frac{\displaystyle\sum_{i=1}^{n} x_i^2 - n\bar{x}^2}{n-1}\]

**Sample Standard Deviation:** \(s = \sqrt{s^2}\) — same units as the data.

**Transformation rule** — if \(y_i = ax_i + b\):
- \(\bar{y} = a\bar{x} + b\)
- \(s_y = |a| \cdot s_x\) — **adding a constant never changes spread!**

> This is exactly A1 Q12: adding 5 marks and rescaling to /80. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/b8409bd7-b7fe-4f60-b454-5d4ff2cb2aee/Assignment-1.pdf)

***

## 📐 Percentiles, Quartiles & IQR

**100p-th percentile** (sort data, compute \(np\)):
- \(np\) **not integer** → \(x_{(\lfloor np \rfloor + 1)}\)
- \(np\) **is integer** → \(\dfrac{x_{(np)} + x_{(np+1)}}{2}\)

| Quartile | = Percentile |
|---|---|
| Q1 | 25th |
| Q2 | 50th (= Median) |
| Q3 | 75th |

\[\text{IQR} = Q3 - Q1\]

**Box plot** shows: Min — Q1 — Median — Q3 — Max [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/be335a48-1a37-4d84-8d8e-7fa9f1b9082a/Topic-1-Descriptive-statistics-Annotated-May-21.pdf)

***

## 📊 Graphs Quick Reference

| Graph | Use when… | Key fact |
|---|---|---|
| **Bar graph / line graph** | Few distinct values | Heights = frequencies |
| **Pie chart** | Categorical (non-numerical) data | Area ∝ relative frequency |
| **Frequency polygon** | Connect **midpoints** of bar tops | |
| **Histogram** | Grouped/continuous data | Bars are **adjacent** |
| **Ogive** | Cumulative rel. frequency | Plotted at **end** of interval ← A1 Q8b trap! |
| **Stem-and-leaf** | Small-moderate numeric data | Preserves raw values |
| **Box plot** | 5-number summary | Min, Q1, Med, Q3, Max |
| **Scatterplot** | Two paired numerical variables | Shows linear trend |

***

## 📐 Sample Correlation Coefficient

\[r = \frac{\displaystyle\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\displaystyle\sum(x_i-\bar{x})^2 \cdot \sum(y_i-\bar{y})^2}}\]

- \(-1 \leq r \leq 1\), unitless
- \(r = \pm 1\): perfect linear relationship
- \(r = 0\): no **linear** relationship (non-linear could still exist!)
- Linear transform \(y_i = ax_i + b\): \(|r|\) unchanged; sign flips only if \(a < 0\)
- **Correlation ≠ Causation** — always suspect lurking/confounding variables [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/be335a48-1a37-4d84-8d8e-7fa9f1b9082a/Topic-1-Descriptive-statistics-Annotated-May-21.pdf)

***

## 📊 Normal vs. Skewed Datasets

| Shape | Tail | Mean vs. Median |
|---|---|---|
| Symmetric (normal) | None | Mean = Median = Mode |
| Right-skewed (+) | Right | Mean > Median |
| Left-skewed (−) | Left | Mean < Median |

***

***

## PART 2 — PROBABILITY & RANDOM VARIABLES (Topic 2, Slides 1–24, Ross Ch. 3 & 4.1–4.2)

***

## 🔑 Probability Interpretations

- **Frequency:** Probability = long-run proportion of times an event occurs
- **Subjective:** Probability = degree of belief in an outcome [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

## 📐 Axioms of Probability

Let \(S\) be the sample space and \(E\) any event:

- **Axiom 1:** \(0 \leq P(E) \leq 1\)
- **Axiom 2:** \(P(S) = 1\)
- **Axiom 3:** For **mutually exclusive** events \(E_1, E_2, \ldots\) (i.e., \(E_i \cap E_j = \emptyset\)):
\[P\!\left(\bigcup_{i=1}^{n} E_i\right) = \sum_{i=1}^{n} P(E_i)\]

**Derived propositions:**
\[P(E^c) = 1 - P(E)\]
\[P(E \cup F) = P(E) + P(F) - P(E \cap F)\]

***

## 📐 Conditional Probability & Bayes

**Conditional Probability:**
\[P(E \mid F) = \frac{P(E \cap F)}{P(F)}, \quad P(F) > 0\]

**Law of Total Probability** (partition \(\{F, F^c\}\)):
\[P(E) = P(E \mid F)\,P(F) + P(E \mid F^c)\,P(F^c)\]

General version (mutually exclusive \(F_1, \ldots, F_n\) covering \(S\)):
\[P(E) = \sum_{i=1}^{n} P(E \mid F_i)\,P(F_i)\]

**Bayes' Formula:**
\[P(F_j \mid E) = \frac{P(E \mid F_j)\,P(F_j)}{\displaystyle\sum_{i=1}^{n} P(E \mid F_i)\,P(F_i)}\]

**Independence:** \(E\) and \(F\) are independent iff:
\[P(E \mid F) = P(E) \quad \Leftrightarrow \quad P(E \cap F) = P(E)\,P(F)\]

> ⚠️ Mutually exclusive ≠ independent. If \(P(E), P(F) > 0\) and they're mutually exclusive, they **can't** be independent. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

## 📐 Random Variables

A **random variable (r.v.)** \(X\) is a numerical quantity determined by a random experiment.

| Type | Takes values in… | Examples |
|---|---|---|
| **Discrete** | Countable set (finite or infinite) | Dice sum, # defective parts |
| **Continuous** | A continuum (interval of reals) | Lifetime, rainfall, temperature |

***

## 📐 CDF — Cumulative Distribution Function

\[F(x) = P(X \leq x)\]

Works for **both** discrete and continuous r.v.'s.

**Key use:**
\[P(a < X \leq b) = F(b) - F(a)\]

**Properties of any CDF:**
- \(0 \leq F(x) \leq 1\)
- Non-decreasing
- \(F(-\infty) = 0\), \(F(+\infty) = 1\)
- Right-continuous (discrete: staircase; continuous: smooth curve) [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

## 📐 PMF — Probability Mass Function (Discrete only)

\[p(x) = P(X = x)\]

- \(p(x) > 0\) only at possible values; \(p(x) = 0\) otherwise
- \(\displaystyle\sum_{\text{all } x} p(x) = 1\)

**CDF from PMF:**
\[F(a) = \sum_{x \leq a} p(x)\]

The CDF is a **right-continuous step function** — it jumps by \(p(x_i)\) at each \(x_i\). [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

## 📐 PDF — Probability Density Function (Continuous only)

\[P(X \in A) = \int_A f(x)\,dx\]

**Key properties:**
- \(f(x) \geq 0\) for all \(x\)
- \(\displaystyle\int_{-\infty}^{+\infty} f(x)\,dx = 1\)
- \(P(a \leq X \leq b) = \displaystyle\int_a^b f(x)\,dx\)
- \(P(X = c) = 0\) for any single point \(c\) ← unique to continuous r.v.'s!

**PDF is the derivative of the CDF:**
\[f(x) = \frac{d}{dx}F(x)\]

**CDF from PDF:**
\[F(x) = \int_{-\infty}^{x} f(t)\,dt\]

> 💡 To find constant \(C\) in a PDF/CDF: use \(F(\text{max}) = 1\) or \(\int_{-\infty}^{+\infty} f(x)\,dx = 1\). [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/152987386/bb695b88-5596-48c1-bc2b-b65c55240a32/Topic-2-Probability-and-random-variables-Annotated-May-28.pdf)

***

## 🧩 PMF / PDF / CDF Relationship Summary

```
Discrete:   p(x) = P(X=x)    →   F(a) = Σ p(x) for x ≤ a
Continuous: f(x) = F'(x)     →   F(a) = ∫ f(x)dx from -∞ to a
Both:       P(a < X ≤ b) = F(b) - F(a)
```

***

## 🚦 Trap Sheet — All Common Mistakes

| Trap | Reality |
|---|---|
| "Ogive plots at midpoint of interval" | ❌ End of interval (A1 Q8b!) |
| "Pie chart works for continuous data" | ❌ Discrete/categorical only (A1 Q8c!) |
| "Tables & graphs = inferential stats" | ❌ They're descriptive (A1 Q3a!) |
| "Surveys = experimental data" | ❌ Surveys = observational (A1 Q3c!) |
| "Large sample = representative sample" | ❌ Must be randomly selected |
| "Adding constant changes std dev" | ❌ Only scaling (\(ax\)) changes spread |
| "\(r=0\) means no relationship" | ❌ No *linear* relationship |
| "Correlation implies causation" | ❌ Always check for confounders |
| "\(P(X=c)=\) something for continuous \(X\)" | ❌ Always 0 for continuous r.v.'s |
| "Mutually exclusive = independent" | ❌ They're actually opposite concepts |
| "Knowing \(F_X\) and \(F_Y\) gives \(F_{XY}\)" | ❌ Need joint CDF for that |