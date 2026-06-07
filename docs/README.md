# SISG26 — Practical 5: Conditional and Joint Analysis (COJO)

> **Summer Institute in Statistical Genetics — Module QG3**  
> Dr. Moeen Riaz · *Original practical: Joelle Mbatchou & Loic Yengo — SISG 2025*

Live site → **[moeenriaz2.github.io/SISG26-downstream-simp](https://moeenriaz2.github.io/SISG26-downstream-simp)**

---

## What is this?

A self-contained R practical on GCTA-COJO (Conditional and Joint analysis), adapted from the [SISG 2025 QG3 Practical 5](https://joellembatchou.github.io/SISG2025_Association_Mapping/QG3_Downstream-Analyses_practical.html) by Joelle Mbatchou and Loic Yengo.

Students simulate a GWAS dataset with known ground-truth causal variants, run GCTA-COJO, and explore how LD reference quality and heritability affect results.

---

## Files

| File | Description |
|------|-------------|
| `index.html` | Landing page |
| `QG3_Downstream-Analyses_practical.html` | The full practical (workflowr-style) |

---

## Practical Structure

| Part | Topic |
|------|-------|
| **Setup** | Download PLINK & GCTA via `setup.sh` from [SISG26-PRS](https://github.com/moeenriaz2/SISG26-PRS) |
| **Part I** | Simulate 1 Mb chromosome · 20 LD blocks · 2,000 SNPs · 100 causal variants |
| **Part II** | Run GCTA-COJO · vary LD reference size (5000 → 500) · vary heritability |
| **Part III** | Apply `--cojo-collinear 0.1` to reduce false positives |

**4 questions** — covering signal detection, LD reference quality, heritability, and collinearity.

---

## Quick Start

```bash
# 1. Clone the tools repo and install PLINK + GCTA
git clone https://github.com/moeenriaz2/SISG26-PRS.git
cd SISG26-PRS
bash setup.sh                      # downloads PLINK 1.9, PLINK 2, GCTB → exe/
export PATH="$PWD/exe:$PATH"
```

```r
# 2. Install required R package
install.packages("MASS")

# 3. Set seed for reproducibility
set.seed(28072023)
```

---

## Deploy to GitHub Pages

1. Upload both files (`index.html` + `QG3_Downstream-Analyses_practical.html`) to this repo
2. **Settings → Pages → Source: main / root → Save**
3. Live at `https://moeenriaz2.github.io/SISG26-downstream-simp`

---

## Credit

- **Joelle Mbatchou & Loic Yengo** — original SISG 2025 QG3 Practical 5
- **Yang J et al.** Conditional and joint multiple-SNP analysis. *Nat Genet* 2012
