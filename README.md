# XAI Práctica 5 — Partial Dependency Plot (PDP)

Práctica de la asignatura **Evaluación de Modelos (EDM)** dedicada a métodos *model-agnostic* de Inteligencia Artificial Explicable (XAI). En concreto, se aplica el **Partial Dependency Plot (PDP)** para interpretar dos modelos de tipo *Random Forest*:

1. **Predicción del alquiler diario de bicicletas** (Bike Sharing Dataset).
2. **Predicción del precio de viviendas** (King County House Sales).

## Estructura del repositorio

```
.
├── data/
│   ├── day.csv             # Bike Sharing - registros diarios
│   ├── hour.csv            # Bike Sharing - registros horarios
│   └── kc_house_data.csv   # King County house sales
├── practica5.Rmd           # Código + análisis (fuente única)
├── practica5.pdf           # Informe compilado
├── enunciado_XAI3.pdf      # Enunciado original de la práctica
└── README.md
```

## Reproducibilidad

Requiere R ≥ 4.0 con los siguientes paquetes:

```r
install.packages(c("randomForest", "ggplot2", "dplyr",
                   "gridExtra", "viridis", "rmarkdown", "knitr", "tinytex"))
tinytex::install_tinytex()   # Solo si no se dispone de una distribución LaTeX
```

Para regenerar el informe:

```r
rmarkdown::render("practica5.Rmd")
```

## Contenido del informe

| Sección | Ejercicio | Descripción |
|---|---|---|
| 1 | PDP 1D (bicicletas) | Random Forest sobre `cnt`. PDP de `days_since_2011`, `temp`, `hum`, `windspeed`. |
| 2 | PDP 2D (bicicletas) | Interacción `humidity` × `temperature` con `geom_tile()` y densidad marginal. |
| 3 | PDP 1D (viviendas) | Random Forest sobre `price`. PDP de `bedrooms`, `bathrooms`, `sqft_living`, `floors`. |

## Autor
- Vizoso Sellem, César Aaron
- Llacer Llorca, Vicente
- Mao, Jiale

elsenyordata — Universidad — Curso 2025/26
