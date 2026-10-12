# Oka water demand forecasting: analysis notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/UDM2202/Water-Demand/blob/main/oka_water_demand_analysis.ipynb)

Code and data behind the paper *Neural network versus regression models for forecasting utility-billed water demand in a data-scarce urban community: a case study of Oka, Benin City, Nigeria* (Ulokaji and Bobor).

**Question.** With 11 annual observations, does an artificial neural network forecast billed water demand better than simple regression?

**Result.** No. Linear regression on population is the most accurate model under leave-one-out and rolling-origin validation. Rainfall, temperature and humidity add no skill. Under central population growth, billed demand is projected at 13.8 million L per year in 2035 (95% prediction interval 12.6 to 15.1).

## Run it

Open `oka_water_demand_analysis.ipynb` in Jupyter, or run it in Google Colab, and run all cells. It takes about three minutes.

```
pip install -r requirements.txt
jupyter notebook oka_water_demand_analysis.ipynb
```

The last cell checks the key results against the values in the paper. A static copy with all outputs is in `oka_water_demand_analysis.html`.

## Files

| File | Contents |
|---|---|
| `oka_water_demand_analysis.ipynb` | Full analysis with outputs: data, models, validation, ANN sensitivity, projection, figures |
| `oka_water_demand_analysis.html` | The same notebook as a web page |
| `data/oka_water_demand_2014_2024.csv` | Annual population, billed demand and climate, 2014 to 2024 |
| `requirements.txt` | Python packages |

## Data notes

Population and utility-billed demand come from the Edo State Urban Water Corporation (EDUWC). The EDUWC annual supply figure (525,600,000 L in every year) is left out because it does not vary. The demand series equals 1.4 to 1.9 litres per person per day, so it represents the volume billed through the utility network and not total household water use. Climate data source: to be added.

## Licence and citation

Code: MIT licence (see `LICENSE`). Data: published with permission from EDUWC.

To cite: add the paper reference and DOI here after publication.
