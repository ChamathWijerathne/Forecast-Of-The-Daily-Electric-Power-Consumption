# Daily Electric Power Consumption Forecasting

Group project for a time-series machine learning course at LUT University (autumn 2025):
forecasting a household's daily electricity use from the
[UCI Individual Household Electric Power Consumption dataset](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)
(about 4 years of one-minute readings, resampled to 1,442 daily values).

## Results

Final model: a Transformer encoder (2 layers, 4 heads, d_model 64) that reads a 30-day window
of 8 daily features and predicts the next 7 days of `y`, the daily average energy not covered
by the three sub-meters (Wh per minute). Chronological 80/20 train/test split, scaler fitted on
training data only.

| Horizon | Day +1 | Day +2 | Day +3 | Day +4 | Day +5 | Day +6 | Day +7 |
|---|---|---|---|---|---|---|---|
| RMSE | 1.91 | 2.04 | 2.14 | 2.21 | 2.26 | 2.30 | 2.77 |
| MAE | 1.39 | 1.56 | 1.60 | 1.67 | 1.70 | 1.69 | 2.02 |

Earlier weeks compared univariate and multivariate RNN and LSTM models, tuning the input
window, batch size and number of epochs (see `notebooks/Week4/` and `multivariate_new.ipynb`).

## Team

| Member | Main work |
|---|---|
| [Chamath Wijerathne](https://github.com/ChamathWijerathne) | EDA, multivariate LSTM experiments, Transformer forecasting model, week 5 report |
| [Nada Rahali](https://github.com/NadaRahali) | Data pretreatment, week 4 univariate and multivariate RNN/LSTM notebooks |
| [Tanjuma Haque](https://github.com/tanjuma) | Group member |

## Repository structure

```
notebooks/
  eda.ipynb                  week 1: visualisation, STL decomposition, autocorrelation
  Data_pretreatment.ipynb    week 2: missing values, interpolation, resampling
  Week4/univariate.ipynb     week 4: univariate RNN/LSTM
  Week4/multivariate.ipynb   week 4: multivariate RNN/LSTM
  multivariate_new.ipynb     week 4, revised after feedback
  transformerNN.ipynb        week 5: first Transformer version
  transformerNN_new.ipynb    week 5: final Transformer model (results above)
docs/
  Week_2_Project_work_2.pdf  data pretreatment report
  Week_5___Project_work_2.pdf  final report
```

## 📊 Dataset Information  

**Source:** [Kaggle - Individual Household Electric Power Consumption Data Set](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)  
**Description:**  
This dataset contains measurements of electric power consumption in a single household with a 1-minute sampling rate over almost 4 years.

**Main Columns Used:**
| Column | Description | Unit |
|---

## Running the notebooks

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

The notebooks download the dataset with `kagglehub`, so a Kaggle account may be needed.
