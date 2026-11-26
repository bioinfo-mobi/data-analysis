# Quiz: Power of a Test
id: power

## Q: In the biomarker diagnostic example, what does β (the Type II error rate) represent?
lang: both
- [ ] The false-positive rate — diagnosing a healthy patient as sick
      β is the Type II error / false-negative rate — failing to detect a real effect.
- [x] The false-negative rate — failing to detect the condition in a patient who actually has it
      Correct! β = false-negative rate, missing a real effect.
- [ ] The proportion of patients tested
      β is the Type II error / false-negative rate — failing to detect a real effect.

## Q: The power of a test is defined as...
lang: both
- [ ] α, the significance level
      Power is 1 − β: the probability of correctly detecting a real effect when it exists.
- [x] 1 − β, the probability of correctly detecting a real effect
      Right! Power = 1 − β = sensitivity.
- [ ] The sample mean
      Power is 1 − β: the probability of correctly detecting a real effect when it exists.

## Q: Which three factors directly influence the statistical power ($1 - \beta$) of a hypothesis test?
lang: both
- [ ] Variable names, color palette, and degree of skewness
      Plot aesthetics do not alter theoretical power.
- [x] Significance level $\alpha$, sample size $n$, and effect size
      Correct! Larger $\alpha$, larger sample sizes $n$, and larger effect sizes all increase the power of a test.
- [ ] Number of outliers, median, and programming language
      Power depends on $\alpha$, sample size $n$, and the true underlying effect size.

## Q: Which of the following would **increase** the power of the diagnostic test in the example?
lang: both
- [ ] Taking fewer measurements per patient (smaller n)
      Larger n shrinks the standard error, making the test more sensitive and increasing power.
- [x] Taking more measurements per patient (larger n), which shrinks the standard error
      Correct! More measurements per patient shrinks SE and increases power.
- [ ] Ignoring the significance level entirely
      Larger n shrinks the standard error, making the test more sensitive and increasing power.

# Quiz: False Positives, False Negatives & FDR (Plenum)
id: errors

## Q: When H0 is actually true, what should the distribution of p-values look like across many repeated tests?
lang: both
- [x] Uniformly distributed between 0 and 1
      Correct! Uniform p-values under H0 is the key validity check for a test.
- [ ] Always exactly 0.05
      Under a valid H0, p-values should be uniformly distributed between 0 and 1.
- [ ] Concentrated near 0
      Under a valid H0, p-values should be uniformly distributed between 0 and 1.

## Q: What is the difference between the False Positive Rate (FPR) and the False Discovery Rate (FDR)?
lang: both
- [ ] They are identical mathematical definitions
      FPR normalizes by all true negatives, while FDR normalizes by all test positives.
- [x] $\text{FPR} = \frac{\text{FP}}{\text{TN} + \text{FP}}$ (proportion of true negatives falsely called significant), while $\text{FDR} = \frac{\text{FP}}{\text{TP} + \text{FP}}$ (proportion of significant calls that are false)
      Correct! FPR controls errors relative to all negative features; FDR controls errors among the discoveries (calls) made.
- [ ] FDR is always fixed at $\alpha = 0.05$
      FDR depends on the proportion of true alternatives and test power, not fixed $\alpha$.

## Q: In the plenum's gene expression simulation (900 genes with no real difference, 100 genes with a real difference), what does the False Discovery Rate (FDR) measure?
lang: both
- [ ] The proportion of all 1000 genes that are truly different
      FDR = false positives divided by all test-positives (genes called "significant").
- [x] The proportion of genes called "significant" (test-positive) that are actually false positives
      Right! FDR looks at test-positives specifically, not all genes.
- [ ] The total number of genes tested
      FDR = false positives divided by all test-positives (genes called "significant").

## Q: Why does the FPR (false-positive rate) stop equaling α when the data is not normally distributed and you still use a t-test?
lang: both
- [x] Because the t-test's theoretical guarantees rely on the normality assumption, which is violated
      Correct! The t-test's FPR = α guarantee depends on the normality assumption.
- [ ] Because software computes p-values incorrectly for non-normal data
      The t-test only controls the FPR at exactly α when its normality assumption holds — violate that, and the guarantee breaks.
- [ ] α always equals the FPR no matter what
      The t-test only controls the FPR at exactly α when its normality assumption holds — violate that, and the guarantee breaks.
