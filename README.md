# Distribution and Confidence Intervals

A hands-on introduction to probability distributions and confidence intervals for data science. The guides and exercises move from identifying and modelling distributions to estimating confidence intervals with both formula-based and bootstrap methods, using worked business and real-world case studies.

## Learning Objectives

By the end of this repository, you should be able to:

- Classify a variable as discrete or continuous and select the distribution (normal, binomial, Poisson, uniform) that models it.
- Compute descriptive statistics (mean, standard deviation, quantiles) and plot a histogram, PMF, PDF, or CDF for a dataset.
- Fit a normal or Poisson distribution to data and calculate event probabilities from it.
- Construct a 95% confidence interval for a mean or proportion using the z/t formula.
- Construct a confidence interval by bootstrapping and measure how it changes with sample size and confidence level.
- Interpret a confidence interval correctly and apply its bounds to make a defined decision.

## Learning Path

### 1 - Distribution

Identify the right distribution for your data and describe it with summary statistics and plots.

| File | Description |
|---|---|
| [**1 - Continuous Distributions Guide**](1_distribution/1_continuous_distributions_guide.ipynb) | Analyse continuous data step by step: identify the data type, frame the question, compute descriptive statistics, and interpret the histogram. |
| [**2 - Discrete Distributions Guide**](1_distribution/2_discrete_distributions_guide.ipynb) | Apply the same analysis loop to discrete count data, with complaints and quality-control case studies. |
| [**3 - Distribution Functions Exercise**](1_distribution/3_distribution_functions_exercise.ipynb) | Practice fitting the normal and Poisson distributions to exam-score, height, and call-volume data. |
| [**Consideration for Distribution Functions**](1_distribution/consideration_for_distribution_function.md) | Cheat sheet: how to choose a distribution, with each one's formulas and scipy syntax. |

### 2 - Confidence Intervals

Estimate a population parameter from a sample and express the uncertainty around it.

| File | Description |
|---|---|
| [**1 - Population Parameters vs Sample Statistics**](2_confidence_intervals/1_population_vs_sample.ipynb) | Recommended pre-reading: the sampling distribution, the standard error, and the central limit theorem that confidence intervals are built on. |
| [**2 - Confidence Intervals Guide**](2_confidence_intervals/2_ci_guide.ipynb) | Populations versus samples, the meaning of a 95% interval, and calculating a confidence interval with both the z/t formula and bootstrapping. |
| [**3 - Confidence Intervals Exercise**](2_confidence_intervals/3_ci_exercise.ipynb) | Interpret and calculate confidence intervals across five case studies, including the Iris dataset. |
| [**Optional**](2_confidence_intervals/optional/) | Optional deep-dive: bootstrap and formula intervals on NYC taxi trip durations, with a statsmodels comparison. |
| [**Data**](2_confidence_intervals/data/) | CSV datasets used in the confidence-interval notebooks. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Solutions**](solutions/) | Reference solutions. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a
> **placeholder**. Replace it, including the `< >` brackets, with your own
> value. For example, `cd <repo-name>` becomes `cd ds-distribution-ci`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Open VS Code from the project root so it detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**Probability distribution (Wikipedia)**](https://en.wikipedia.org/wiki/Probability_distribution): A broad reference on distributions and their terminology.
- [**scipy.stats reference**](https://docs.scipy.org/doc/scipy/reference/stats.html): The distributions and statistical functions used throughout these notebooks.
- [**NumPy random sampling**](https://numpy.org/doc/stable/reference/random/index.html): Generating samples from distributions, the basis of bootstrapping.
- [**seaborn: visualising distributions**](https://seaborn.pydata.org/tutorial/distributions.html): Histograms, density plots, and ECDFs for exploring data.
- [**From Data to Viz**](https://www.data-to-viz.com/): A decision tree for choosing the right chart, with a strong section on visualising distributions and common pitfalls.
- [**ModernDive: Confidence Intervals and Bootstrapping**](https://moderndive.com/v2/confidence-intervals.html): A data-science treatment of confidence intervals built on the bootstrap.
