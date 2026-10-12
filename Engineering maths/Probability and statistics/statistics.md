                    STATISTICS
Statistics is the branch of mathematics concerned with collecting, organizing, presenting, analyzing, and interpreting data to make decisions under uncertainty.

Engineering applications:
- Quality control and manufacturing.
- Analysis of experimental results.
- Reliability and performance testing.
- Measurement uncertainty and error analysis.
- Process optimization and predictive modelling.

Basic Terminology:
- Population: The entire group of items or observations under investigation.
- Sample: A subset selected from the population.
- Parameter: A numerical characteristic of a population, e.g., μ or σ².
- Statistic: A numerical quantity calculated from sample data, e.g., x̄ or s².
- Variable: A characteristic measured or observed.
- Qualitative data: Categories, e.g., material type.
- Quantitative data: Numerical values, e.g., voltage or length.
- Discrete data: Countable numerical values.
- Continuous data: Measurements that can take values over an interval.
- Frequency: Number of observations in a category or class.
- Outlier: An observation unusually far from the main data pattern.

Data Collection and Sampling:
    Common sampling methods:
1. Simple random sampling: Each population member has an equal chance of selection.
2. Systematic sampling: Select every kth item after a suitable starting point.
3. Stratified sampling: Divide the population into groups and sample from each.
4. Cluster sampling: Select groups or clusters and observe their members according to the sampling design.
A representative sample reduces selection bias. Larger samples generally improve precision under appropriate conditions, but do not automatically eliminate bias.

Presentation of Data:
    Common methods include:
- Frequency tables.
- Bar charts for categories.
- Histograms for numerical distributions.
- Pie charts for proportions.
- Frequency polygons.
- Ogives (cumulative frequency curves).
- Scatter plots for relationships between two numerical variables.
- Box plots for medians, quartiles, and potential outliers.
For grouped data, class midpoint:
    m = (Lower class limit + Upper class limit)/2
Relative frequency:
    Relative frequency = Frequency / Total frequency
Percentage frequency:
    Percentage frequency = Relative frequency × 100%
Cumulative frequency is the running total of frequencies.

Measures of Central Tendency:
These describe the centre of a dataset.
    A. Arithmetic mean
        For raw data:
            x̄ = Σxᵢ/n
        For a frequency distribution:
            x̄ = Σfᵢxᵢ / Σfᵢ
        where xᵢ represents a value or class midpoint and fᵢ its frequency.
    B. Median
        The middle observation after sorting the data.
        - Odd n: Median is the observation at position (n + 1)/2.
        - Even n: Median is the average of observations at positions n/2 and n/2 + 1.
        For grouped continuous data, an approximate median is:
            Median = L + [(N/2 − C)/f]h
        where:
            - L = lower boundary of the median class.
            - N = total frequency.
            - C = cumulative frequency before the median class.
            - f = frequency of the median class.
            - h = class width.
    C. Mode
        The most frequently occurring value.
        For grouped data, an approximate mode is:
            Mode = L + [d₁/(d₁ + d₂)]h
        where:
            - L = lower boundary of the modal class.
            - d₁ = modal class frequency − preceding class frequency.
            - d₂ = modal class frequency − succeeding class frequency.
            - h = class width.
When to use:
    - Mean: useful for numerical analysis but sensitive to outliers.
    - Median: useful for skewed data or data containing outliers.
     - Mode: useful for identifying the most common value or category.

Measures of Dispersion:
Dispersion describes how spread out observations are.
    A. Range
        Range = Maximum value − Minimum value
    B. Population variance
        σ² = Σ(xᵢ − μ)²/N
    C. Sample variance
        s² = Σ(xᵢ − x̄)²/(n − 1)
        The sample variance uses n − 1 in the denominator when estimating population variance from a sample using the sample mean.
        Computational formula for sample variance:
        s² = [Σxᵢ² − (Σxᵢ)²/n]/(n − 1)  
    D. Standard deviation
        Population: σ = √σ²
        Sample: s = √s²
        Standard deviation is expressed in the same units as the original measurements.
    E. Quartiles and interquartile range
        - Q₁: Lower quartile.
        - Q₂: Median.
        - Q₃: Upper quartile.
        IQR = Q₃ − Q₁
        The IQR describes the spread of the middle 50% of observations.
        A common rule for flagging potential outliers is:
            Lower fence = Q₁ − 1.5(IQR)
            Upper fence = Q₃ + 1.5(IQR)
        Values outside these fences are potential outliers, not necessarily errors.
    F. Coefficient of variation
            CV = (s/x̄) × 100%
        For a population, CV = (σ/μ) × 100%, where the mean is meaningfully positive.
        The CV compares relative variability between datasets measured on a suitable ratio scale.

Measures of Position and Shape:
Z-score:
    z = (x − μ)/σ
    For sample-based standardization, z-scores may instead use x̄ and s.
    A z-score indicates how many standard deviations a value lies above or below the mean.
Skewness:
    - Zero skewness: symmetric distribution in the usual interpretation.
    - Positive skewness: longer right tail.
    - Negative skewness: longer left tail.
Kurtosis: Describes aspects of tail weight and distribution shape relative to a reference distribution; definitions vary by convention.

Probability Distributions in Statistics:
Statistics uses probability distributions to model data and quantify uncertainty.
Important distributions include:
    - Binomial: Number of successes in a fixed number of independent trials.
    - Poisson: Counts of events over a specified interval.
    - Normal: Continuous measurements and many statistical approximations.
    - Student's t: Inference about a population mean when the population standard deviation is unknown under appropriate assumptions.
    - Chi-square: Categorical-data tests and inference about variance under suitable assumptions.
    - F-distribution: Variance comparisons and analysis of variance (ANOVA).

Sampling Distributions and the Central Limit Theorem:
A sampling distribution describes the distribution of a statistic across repeated samples.
For independent observations with population mean μ and finite variance σ²:
    E(x̄) = μ
    Var(x̄) = σ²/n
Standard error of the sample mean:
    SE(x̄) = σ/√n
    When σ is unknown, it is commonly estimated using:
    SE(x̄) ≈ s/√n
Central Limit Theorem (CLT): Under suitable conditions, the sampling distribution of the sample mean approaches a normal distribution as the sample size increases, even when the underlying population is not normal.
The required sample size depends on the population distribution and the statistic being studied.

Estimation and Confidence Intervals:
A point estimate uses a single value to estimate a population parameter.
Examples:
    - x̄ estimates μ.
    - s² estimates σ².
    - p̂ estimates a population proportion p.
Confidence interval for a population mean when σ is known:
    x̄ ± z₁₋α/₂(σ/√n)
Confidence interval for a population mean when σ is unknown:
    x̄ ± t₁₋α/₂, n₋₁(s/√n)
Use the t-distribution when its assumptions are appropriate, especially for a normal population with unknown standard deviation.
For a large-sample proportion under suitable conditions:
    p̂ ± z₁₋α/₂√[p̂(1 − p̂)/n]
Common two-sided normal critical values:
    - 90% confidence: z ≈ 1.645.
    - 95% confidence: z ≈ 1.96.
    - 99% confidence: z ≈ 2.576.
A 95% confidence procedure captures the true parameter in 95% of repeated samples in the long run, under the model assumptions. It does not mean there is a 95% probability that a fixed parameter lies in a particular calculated frequentist interval.

Hypothesis Testing:
Hypothesis testing evaluates evidence about a population parameter.
Null hypothesis (H₀): The baseline claim being tested.
Alternative hypothesis (H₁ or Hₐ): The competing claim.
Significance level (α): The chosen probability of a Type I error, commonly 0.05.
Type I error: Rejecting a true null hypothesis.
Type II error: Failing to reject a false null hypothesis.
p-value: The probability, assuming H₀ and the model assumptions are true, of observing a test statistic at least as extreme as the one obtained in the direction(s) specified by the test.
Decision rule:
    - If p-value ≤ α, reject H₀.
    - If p-value > α, fail to reject H₀.
Do not interpret failure to reject H₀ as proof that H₀ is true.
One-sample z-test for a mean when σ is known:
    z = (x̄ − μ₀)/(σ/√n)
One-sample t-test for a mean when σ is unknown:
    t = (x̄ − μ₀)/(s/√n)
Degrees of freedom = n − 1.
A one-tailed test evaluates a directional alternative; a two-tailed test evaluates a difference in either direction. Choose the test direction before examining the results.

Correlation and Regression:
Correlation coefficient (Pearson's r):
    r = Σ[(xᵢ − x̄)(yᵢ − ȳ)] / √{Σ(xᵢ − x̄)² Σ(yᵢ − ȳ)²}
    −1 ≤ r ≤ 1
    - r near +1: strong positive linear association.
    - r near −1: strong negative linear association.
    - r near 0: weak or absent linear association.
Correlation does not establish causation.
Simple linear regression:
    ŷ = a + bx
    where:
        - ŷ = predicted response.
        - a = intercept.
        - b = slope.
        - x = explanatory variable.
    Slope:
        b = Σ[(xᵢ − x̄)(yᵢ − ȳ)] / Σ(xᵢ − x̄)²
    Intercept:
        a = ȳ − bx̄
Regression models relationships and supports prediction within the limits of the data and model assumptions. Extrapolation beyond the observed range may be unreliable.

Engineering Applications: Quality Control:
Control charts help monitor process variation over time.
For an individuals or subgroup-based process, chart selection depends on the data type and sampling design.
Common charts:
    - X̄-chart: monitors subgroup means.
    - R-chart: monitors subgroup ranges.
    - p-chart: monitors the fraction defective.
    - c-chart: monitors defect counts when the opportunity for defects is constant.
Control limits are calculated from the relevant process model. They are not automatically the same as specification limits, which describe acceptable product requirements.

Worked Examples:
    Example 1: Mean and range
        Data: 2, 4, 4, 6, 9
        Mean: x̄ = (2 + 4 + 4 + 6 + 9)/5 = 5
        Range = 9 − 2 = 7
        Median = 4
        Mode = 4
    Example 2: Sample variance and standard deviation
        Using the same data, x̄ = 5.
        Squared deviations:
            (2 − 5)² + (4 − 5)² + (4 − 5)² + (6 − 5)² + (9 − 5)²
            = 9 + 1 + 1 + 1 + 16 = 28
        Sample variance:
            s² = 28/(5 − 1) = 7
        Sample standard deviation:
            s = √7 ≈ 2.65
    Example 3: Standard error
        A sample has standard deviation s = 12 and sample size n = 36.
            SE(x̄) = s/√n = 12/6 = 2
    Example 4: Linear regression
Suppose a fitted model relating temperature x to a measured response is:
    ŷ = 5 + 2x
    At x = 10:
    ŷ = 5 + 2(10) = 25
The prediction is valid only to the extent that the fitted relationship is appropriate for the input and operating conditions.

Problem-Solving Tips:
1. Identify whether the data describe a population or a sample.
2. Sort raw data before calculating the median or quartiles.
3. Use n − 1 for the usual unbiased sample-variance estimator.
4. Distinguish variance (squared units) from standard deviation (original units).
5. Use the mean and standard deviation for suitable approximately symmetric data; use the median and IQR when outliers or skewness make them more appropriate.
6. Check assumptions before using a normal approximation, confidence interval, or hypothesis test.
7. Report confidence intervals alongside estimates when useful.
8. A statistically significant result is not necessarily practically or economically significant.
9. Correlation measures association, not causation.
10. Distinguish process control limits from engineering specification limits.
11. Present results with appropriate units, rounding, and a clear interpretation.