## Introduction to Distributions

   - **Definition:** A distribution represents the pattern or arrangement of data values in a dataset. It shows how often each value occurs and the range of values within the dataset.

   - **Purpose:** Distributions provide insights into the central tendency (mean, median, mode) and variability (spread) of data, making them essential for data analysis and modeling.

   - **Common Terms:** 
      - **Probability Density Function (PDF):** For continuous distributions, PDF defines the probability of observing a specific value. It represents the density of the data at each point in the distribution. *Probabilities of continuous random variables (X) are defined as the area under the curve of its PDF*.
      - **Probability Mass Function (PMF):** For discrete distributions, PMF assigns probabilities to individual values. It gives the probability of observing each discrete value in the distribution.
      - **Cumulative Distribution Function (CDF):** Shows the probability that a random variable takes on a value less than or equal to a given value.

## Probability Density Function (PDF) for Discrete Random Variables

**1. Definition:**
   - A Probability Density Function (PDF) for a discrete random variable is a mathematical function that assigns probabilities to each possible outcome of the random variable.
   - The PDF describes the likelihood of each specific value occurring in a discrete probability distribution.

**2. Notation:**
   - Denoted as \(P(X = x)\), where \(X\) is the random variable and \(x\) is a specific value of that variable.
   - Alternatively, it can be represented by \(f(x)\).

**3. Properties:**
   - **Non-negative:** \(P(X = x)\) is always greater than or equal to zero for all \(x\).
   - **Sum of Probabilities:** The sum of probabilities for all possible values of \(X\) equals 1: \(\sum P(X = x) = 1\).

**4. Example:**
   - Consider a six-sided fair die roll. The PDF would be:
      - \(P(X = 1) = 1/6\)
      - \(P(X = 2) = 1/6\)
      - \(P(X = 3) = 1/6\)
      - \(P(X = 4) = 1/6\)
      - \(P(X = 5) = 1/6\)
      - \(P(X = 6) = 1/6\)

**5. Probability Mass Function (PMF):**
   - For discrete random variables, the PDF is also called the Probability Mass Function (PMF).
   - The PMF provides the probability of each individual outcome and can be used to calculate the expected value and variance of the random variable.

### Types of Discrete Probability Distributions
Certainly! Here are in-depth notes on some common types of discrete probability distributions:

#### 1. **Bernoulli Distribution**

   - **Definition:**
      - The Bernoulli distribution models a single trial with two possible outcomes: success (usually denoted as 1) and failure (usually denoted as 0).

   - **Parameters:** 
      - Probability of success, denoted as \(p\).
      - Probability of failure, denoted as \(q = 1 - p\).

   - **Probability Mass Function (PMF):**
      - \(P(X = 1) = p\)
      - \(P(X = 0) = q\)

   - **Mean and Variance:**
      - Mean (Expected Value): \(E(X) = p\)
      - Variance: \(Var(X) = pq\)

   - **Applications:** 
      - Modeling binary events like coin flips (head or tail).
      - Representing success or failure in a single trial (e.g., pass/fail experiments).

#### 2. **Binomial Distribution**

   - **Definition:**
      - The binomial distribution models the number of successes (X) in a fixed number (n) of independent Bernoulli trials.

   - **Parameters:** 
      - Number of trials, \(n\).
      - Probability of success in each trial, \(p\).

   - **Probability Mass Function (PMF):**
      - \(P(X = k) = \binomial{n}{k} p^k (1-p)^{n-k}\)

   - **Mean and Variance:**
      - Mean (Expected Value): \(E(X) = np\)
      - Variance: \(Var(X) = npq\)

   - **Applications:** 
      - Modeling the number of successes in a fixed number of independent trials (e.g., number of heads in multiple coin flips).
      - Analyzing the outcomes of repeated independent experiments.

#### 3. **Poisson Distribution**

   - **Definition:**
      - The Poisson distribution models the number of events occurring in a fixed interval of time or space, assuming these events happen independently at a constant average rate.

   - **Parameter:** 
      - Average rate or mean number of events, denoted as \(\lambda\).

   - **Probability Mass Function (PMF):**
      - \(P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}\)

   - **Mean and Variance:**
      - Mean (Expected Value): \(E(X) = \lambda\)
      - Variance: \(Var(X) = \lambda\)

   - **Applications:** 
      - Modeling rare events like accidents, the number of phone calls received at a call center in a fixed time period, or the number of emails received per hour.
      - Analyzing count data in various fields, such as epidemiology and finance.

#### 4. **Geometric Distribution**

   - **Definition:**
      - The geometric distribution models the number of Bernoulli trials needed to achieve the first success.

   - **Parameter:** 
      - Probability of success in each trial, \(p\).

   - **Probability Mass Function (PMF):**
      - \(P(X = k) = (1-p)^{k-1}p\)

   - **Mean and Variance:**
      - Mean (Expected Value): \(E(X) = \frac{1}{p}\)
      - Variance: \(Var(X) = \frac{1-p}{p^2}\)

   - **Applications:** 
      - Modeling the number of trials required until a success (e.g., the number of coin flips until the first heads).
      - Analyzing situations involving repeated independent trials until a desired outcome occurs.

#### 5. **Hypergeometric Distribution**

   - **Definition:**
      - The hypergeometric distribution models the number of successes (X) in a sample drawn from a finite population without replacement.

   - **Parameters:** 
      - Population size, \(N\).
      - Number of successes in the population, \(K\).
      - Sample size, \(n\).

   - **Probability Mass Function (PMF):**
      - \(P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}\)

   - **Mean and Variance:**
      - Mean (Expected Value): \(E(X) = \frac{nK}{N}\)
      - Variance: \(Var(X) = \frac{nK(N-K)(N-n)}{N^2(N-1)}\)

   - **Applications:** 
      - Modeling situations like drawing a certain number of defective items from a batch, selecting specific individuals from a population, etc.
      - Addressing sampling without replacement scenarios.




## Probability Density Function (PDF) for Continuous Random Variables

**1. Definition:**
   - A Probability Density Function (PDF) for a continuous random variable is a mathematical function that describes the probability distribution for continuous data.
   - Unlike the discrete case, where each value has a probability, the PDF for continuous random variables gives probabilities over intervals.

**2. Notation:**
   - Typically denoted as \(f(x)\).
   - For a continuous random variable \(X\), \(P(X = x) = 0\) for any specific value \(x\).

**3. Properties:**
   - **Non-negative:** \(f(x)\) is always non-negative for all \(x\).
   - **Total Area Under the Curve:** The total area under the PDF curve over the entire range of possible values is equal to 1.

**4. Example:**
   - The PDF for a standard normal distribution (bell-shaped curve) is given by the following formula:
```math
\(f(x) = \frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}x^2}\) 
```

**5. Probability over Intervals:**
   - Since continuous random variables can take on any real value within a range, the PDF provides the probability that the variable falls within a specified interval.
   - Probability is calculated as the integral of the PDF over that interval.

**6. Mean and Variance:**
   - The mean (expected value) and variance of a continuous random variable can be calculated using the PDF:
      - Mean: \(E(X) = \int_{-\infty}^{\infty} x \cdot f(x) \,dx\)
      - Variance: \(Var(X) = \int_{-\infty}^{\infty} (x - E(X))^2 \cdot f(x) \,dx\)


### Types of Continuous Probability Distributions

#### 1. **Normal Distribution (Gaussian Distribution)**

   - **Definition:** The normal distribution is a continuous probability distribution characterized by its bell-shaped curve. It is symmetric and unimodal, with the mean (μ) at the center.

   - **Parameters:** 
      - Mean (μ) determines the center of the distribution.
      - Standard Deviation (σ) controls the spread or dispersion.

   - **Probability Density Function (PDF):**
      - \(f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma^2}}\)

   - **Properties:**
      - Approximately 68% of data falls within one standard deviation of the mean (μ ± σ).
      - Approximately 95% falls within two standard deviations (μ ± 2σ).
      - About 99.7% falls within three standard deviations (μ ± 3σ).
   
   - **Applications:** 
      - Many natural phenomena follow the normal distribution (e.g., heights, IQ scores).
      - Central to the field of statistics and hypothesis testing.

#### 2. **Uniform Distribution**

   - **Definition:** The uniform distribution is characterized by a constant probability density over a fixed interval.

   - **Parameters:** 
      - Lower bound (a) and upper bound (b) of the interval.

   - **Probability Density Function (PDF):**
      - \(f(x) = \frac{1}{b-a}\) for \(a \leq x \leq b\)
      - \(f(x) = 0\) elsewhere.

   - **Properties:**
      - All values within the interval are equally likely.

   - **Applications:** Modeling situations where each outcome in an interval is equally probable, such as random number generation.

#### 3. **Exponential Distribution**

   - **Definition:** The exponential distribution models the time between events in a Poisson process, where events occur independently at a constant average rate.

   - **Parameter:** 
      - Rate parameter (λ), which represents the average number of events in a unit of time.

   - **Probability Density Function (PDF):**
      - \(f(x) = \lambda e^{-\lambda x}\) for \(x \geq 0\)
      - \(f(x) = 0\) for \(x < 0\)

   - **Properties:**
      - Right-skewed with a long tail.
      - The mean (\(E(X)\)) is \(1/\lambda\), and the variance (\(Var(X)\)) is \(1/\lambda^2\).

   - **Applications:** Modeling the time between arrivals of customers at a service center, time between phone calls, or radioactive decay.

#### 4. **Log-Normal Distribution**

   - **Definition:** The log-normal distribution describes data that follows a multiplicative process and is characterized by a right-skewed curve after taking the natural logarithm.

   - **Parameters:** 
      - Mean (μ) and standard deviation (σ) of the natural logarithm of the data.

   - **Probability Density Function (PDF):**
      - \(f(x) = \frac{1}{x\sigma\sqrt{2\pi}} e^{-\frac{(\ln(x) - \mu)^2}{2\sigma^2}}\) for \(x > 0\)

   - **Properties:**
      - The original data is positively skewed.
      - Often used in finance for modeling stock prices and in income distribution studies.

   - **Applications:** Modeling data that exhibits exponential growth, such as financial data or sizes of biological organisms.

#### 5. **Gamma Distribution**

   - **Definition:** The gamma distribution is a family of continuous probability distributions that generalizes the exponential distribution.

   - **Parameters:** 
      - Shape parameter (k) and rate parameter (λ).

   - **Probability Density Function (PDF):**
      - \(f(x; k, \lambda) = \frac{\lambda^k}{\Gamma(k)} x^{k-1} e^{-\lambda x}\) for \(x > 0\)

   - **Properties:**
      - Can model waiting times until a fixed number of Poisson events occur.
      - Includes the exponential distribution as a special case when \(k = 1\).

   - **Applications:** Modeling various continuous data, including time until machine failures, arrival times in queues, and rainfall amounts.

#### 6. **Beta Distribution**

   - **Definition:** The beta distribution is a family of continuous probability distributions defined on the interval [0, 1].

   - **Parameters:** 
      - Shape parameters α and β.

   - **Probability Density Function (PDF):**
      - \(f(x; \alpha, \beta) = \frac{1}{\text{B}(\alpha, \beta)} x^{\alpha-1} (1-x)^{\beta-1}\) for \(0 \leq x \leq 1\)

   - **Properties:**
      - Flexible distribution useful for modeling proportions, probabilities, and random variables constrained to a finite range.
      - The uniform distribution is a special case when α = β = 1.

   - **Applications:** Modeling probabilities, random variables representing proportions, and Bayesian inference.
#### 7. **Student's t Distribution**

   - **Definition:** The Student's t distribution, often referred to as the t-distribution, is used to model the distribution of sample means when the population standard deviation is unknown and must be estimated from the sample.

   - **Parameters:** 
      - Degrees of Freedom (df), which determine the shape of the distribution.

   - **Probability Density Function (PDF):**
      - \(f(x; df) = \frac{\Gamma(\frac{df+1}{2})}{\sqrt{df\pi}\Gamma(\frac{df}{2})} \left(1 + \frac{x^2}{df}\right)^{-\frac{df+1}{2}}\)

   - **Properties:**
      - Symmetric and bell-shaped.
      - As the degrees of freedom increase, the t-distribution approaches the standard normal distribution.
   
   - **Applications:** 
      - Commonly used in hypothesis testing when the population standard deviation is unknown.
      - Inferences about population means when sample size is small.

#### 8. **Chi-square Distribution**

   - **Definition:** The Chi-square distribution is used to model the sum of squared independent standard normal random variables.

   - **Parameters:** 
      - Degrees of Freedom (df), which determine the shape of the distribution.

   - **Probability Density Function (PDF):**
      - \(f(x; df) = \frac{1}{2^{\frac{df}{2}}\Gamma(\frac{df}{2})} x^{\frac{df}{2}-1} e^{-\frac{x}{2}}\)

   - **Properties:**
      - Right-skewed and unimodal.
      - As the degrees of freedom increase, the Chi-square distribution approaches a normal distribution.
   
   - **Applications:** 
      - Commonly used in hypothesis testing for comparing variances or testing goodness of fit.
      - In the construction of confidence intervals for the population variance.

#### 9. **F Distribution**

   - **Definition:** The F distribution is used to model the ratio of two independent Chi-square distributed random variables, each divided by their respective degrees of freedom.

   - **Parameters:** 
      - Degrees of Freedom for the numerator (\(df_1\)) and denominator (\(df_2\)).

   - **Probability Density Function (PDF):**
      - \(f(x; df_1, df_2) = \frac{\Gamma(\frac{df_1+df_2}{2})}{\Gamma(\frac{df_1}{2})\Gamma(\frac{df_2}{2})} \left(\frac{df_1}{df_2}\right)^{\frac{df_1}{2}} \frac{x^{\frac{df_1}{2}-1}}{(1+\frac{df_1}{df_2}x)^{\frac{df_1+df_2}{2}}}\)

   - **Properties:**
      - Right-skewed and unimodal.
      - Widely used in statistical tests, such as analysis of variance (ANOVA) and regression analysis.
   
   - **Applications:** 
      - Comparing variances of two populations.
      - Assessing the significance of regression models.
      - Hypothesis testing in ANOVA.
