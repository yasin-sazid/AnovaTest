# ANOVA of Developer Compensation

An exploratory statistics notebook investigating compensation differences among ethnicity groups in developer survey data. The project connects data preparation, visual diagnostics, and hypothesis testing in one reproducible analytical narrative.

## Analytical workflow

1. Load the `Ethnicity` and `ConvertedComp` columns from a survey CSV.
2. Remove incomplete observations and scale compensation to the interval from zero to one.
3. Explore the distribution with histograms and Q–Q plots.
4. Apply interquartile-range filtering and a square-root transformation.
5. Construct White/European, Black/African, and East Asian groups using the survey's ethnicity responses.
6. Examine group dispersion with Levene's test and box plots, then calculate one-way ANOVA with SciPy's `f_oneway`.

The notebook makes the preparation steps visible alongside the statistical calculations, illustrating how distributional assumptions and grouping choices enter an applied analysis. Ethnicity matching uses substring membership, so a multi-selection survey response can participate in more than one group.

## Explore the notebook

Open [1006_anova.ipynb](1006_anova.ipynb) in Jupyter Notebook or JupyterLab. Use a Python environment containing NumPy, pandas, SciPy, seaborn, statsmodels, and Matplotlib:

```bash
python -m pip install jupyter numpy pandas scipy seaborn statsmodels matplotlib
jupyter notebook 1006_anova.ipynb
```

Supply `survey_results_public.csv` with the two required columns at the location referenced by the notebook's loading cell. Execute cells in order to follow preprocessing, visual inspection, and statistical output. The notebook preserves the original analysis and its recorded observations.

## Technologies

Python · Jupyter · pandas · NumPy · SciPy · statsmodels · seaborn · Matplotlib
