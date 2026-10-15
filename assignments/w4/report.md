## Objective Statement

After Hurricane Katrina, some residents of Biloxi, Mississippi, did not rebuild their homes. The city planned to put redevelopment funds into the neighborhood with the lowest proportion of rebuilt lots, but it did not know which neighborhood had the lowest population proportion. The objective was to calculate a 95% confidence interval for the proportion of rebuilt lots in East, West, and North Biloxi and to compare the intervals to recommend where the city should direct its funds.

## Methods

The data came from the City of Biloxi Redevelopment Survey, adapted from data collected by Dr. Christopher Burton of the Auburn University Department of Geosciences. The dataset contained 90 records: 30 randomly selected lots from each of East, West, and North Biloxi. The variables were Neighborhood, Lot Number, and Rebuilt (1 for rebuilt, 0 for vacant). Because each lot had a yes-or-no outcome, a confidence interval for a proportion was used to estimate each neighborhood's true proportion of rebuilt lots. In Excel, the number of lots sampled in each neighborhood (n) was found with COUNTIF, and the number of rebuilt lots (x) was found with SUMIF. The sample proportion (p̂) was calculated with Equation 1.

EQUATION: p̂ = x / n   (1)

The 95% confidence interval used Equation 2, where z* was the critical value and the square root term was the standard error (SE), computed with SQRT.

EQUATION: CI = p̂ ± z* √( p̂(1 − p̂) / n )   (2)

NORM.S.INV(0.975) gave z* = 1.960. The margin of error (ME) was z* multiplied by SE, and the bounds were p̂ minus ME and p̂ plus ME. A proportion cannot exceed 1, so the upper bound was limited with MIN(1, upper bound). The normal approximation was checked by confirming that n·p̂ and n(1 − p̂) were each at least 5.

## Results and Conclusions

East and West Biloxi had the lowest proportions of rebuilt lots, but the data could not show which of the two was lower. The sample proportion of rebuilt lots was 0.700 in East Biloxi (95% CI 0.536 to 0.864), 0.767 in West Biloxi (95% CI 0.615 to 0.918), and 0.967 in North Biloxi (95% CI 0.902 to 1.000) (Table 1). The East and West intervals overlapped substantially, while North's interval did not overlap East's and overlapped West's only from 0.902 to 0.918.

If sampling had been repeated many times, about 95% of intervals built this way would have contained the true proportion, so we were 95% confident that the true proportion of rebuilt lots in each neighborhood fell within its interval. Since the East and West intervals overlapped, either neighborhood could have had the lower true proportion. Every plausible value for North was at least 0.902, which was above all of East's interval and above all but the top edge of West's, so North did not meet the city's criterion of having the lowest rebuilt proportion. The North interval was less reliable than the others because n(1 − p̂) was only 1, which failed the normal approximation condition, but this did not change the comparison. The results supported directing redevelopment funds to East and West Biloxi instead of North Biloxi. If only one neighborhood could be funded, East Biloxi was the best choice based on its point estimate, although a larger sample would be needed to confirm that its proportion was lower than West Biloxi's.

TABLE 1 CAPTION: Table 1. Sample proportions and 95% confidence intervals for the proportion of rebuilt lots in three Biloxi neighborhoods (City of Biloxi Redevelopment Survey).

| Neighborhood | Lots sampled (n) | Lots rebuilt (x) | Sample proportion (p̂) | Margin of error | 95% CI lower bound | 95% CI upper bound |
|---|---|---|---|---|---|---|
| East Biloxi | 30 | 21 | 0.700 | 0.164 | 0.536 | 0.864 |
| West Biloxi | 30 | 23 | 0.767 | 0.151 | 0.615 | 0.918 |
| North Biloxi | 30 | 29 | 0.967 | 0.064 | 0.902 | 1.000 |

TABLE NOTE: The North Biloxi upper bound was calculated as 1.031 and was capped at 1.000 with MIN. For North Biloxi, n(1 − p̂) was 1, below 5, so the normal approximation was weak and the interval was interpreted with caution.
