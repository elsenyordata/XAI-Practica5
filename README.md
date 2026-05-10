# XAI Practice 5 — Partial Dependency Plot (PDP)

Practice for the subject **Model Evaluation (EDM)** focused on *model-agnostic* methods of Explainable Artificial Intelligence (XAI). Specifically, the **Partial Dependency Plot (PDP)** is applied to interpret two *Random Forest* models:

1. **Daily bike rental prediction** (Bike Sharing Dataset).
2. **House price prediction** (King County House Sales).

## Repository structure

```
.
├── data/
│   ├── day.csv             # Bike Sharing - daily records
│   ├── hour.csv            # Bike Sharing - hourly records
│   └── kc_house_data.csv   # King County house sales
├── practica5.Rmd           # Code + analysis (single source)
├── practica5.pdf           # Compiled report(SPANISH)
├── enunciado_XAI3.pdf      # Original practice statement
--->ENTREGABLE_XAI3.pdf  #FINAL REPORT IN ENGLISH
└── README.md
```

## Reproducibility

Requires R ≥ 4.0 with the following packages:

```r
install.packages(c("randomForest", "ggplot2", "dplyr",
                   "gridExtra", "viridis", "rmarkdown", "knitr", "tinytex"))
tinytex::install_tinytex()   # Only if no LaTeX distribution is available
```

To regenerate the report:

```r
rmarkdown::render("practica5.Rmd")
```

## Report content

| Section | Exercise | Description |
|---|---|---|
| 1 | 1D PDP (bikes) | Random Forest on `cnt`. PDP of `days_since_2011`, `temp`, `hum`, `windspeed`. |
| 2 | 2D PDP (bikes) | `humidity` × `temperature` interaction with `geom_tile()` and marginal density. |
| 3 | 1D PDP (houses) | Random Forest on `price`. PDP of `bedrooms`, `bathrooms`, `sqft_living`, `floors`. |

## Authors
- Vizoso Sellem, César Aaron
- Llacer Llorca, Vicente
- Mao, Jiale

Universitat Politècnica de València — GCD — Academic year 2025/26
