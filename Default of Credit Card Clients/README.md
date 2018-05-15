# Default of Credit Card Clients

\*To see this on Kaggle, click [here](https://www.kaggle.com/melindaleung/default-of-credit-card-clients).

This [dataset](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients) comes from the UCI Machine Learning Repository. It contains information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005. The goal of this proposal is to determine the strongest predictors of default payments and to examine the probability of default payment in relation to various categories of demographic variables. Using this information, I will provide a recommendation on how to lower the rate of default payment.

### Background

Credit card default is the failure to meet the legal obligations of a credit card, like paying your credit card in a timely manner. This not only lowers your credit score, but affects your ability to get approved for other credit cards, loans, and other credit-based services. 

Back in 2005, Taiwan faced a large cash and credit card debt crisis. Card-issuing banks over-issued cash and credit cards to unqualified applicants while cardholders overused credit card consumption and accumulated large debts. By February 2006, debt from credit and cash cards reached 268 billion dollars; more than half a million people were not able to repay their loans. 

This crisis not only hurt the financial system, but also resulted in significant societal problems. Many debtors committed suicide, some became homeless, and other's no longer could afford sending their children to school. People began resorting to illegal drug sales. In addition, violent and treatening collection practices added additional pressure. According to the Taiwanese Department of Health, 4,406 committed suicide in 2006 (which was a 22.9 percent increase from 2005). Suicide rates in Taiwain are the second highest in the world and the main reason often is unemployment and credit card debt.

Credit card debt can lead to serious financial and societal issues. In order to prevent this from happening again, it is important to examine past credit card information to determine who are high risk borrows. Therefore, the government can effectively devise a solution to resolve this problem. 

*Source: [Taiwan's Credit Card Crisis](https://sevenpillarsinstitute.org/case-studies/taiwans-credit-card-crisis/) by Eric Wang*

### Problem Statement

How do you predict if a cardholder is likely to default on their credit card? What are the strongest predictors of default payment? What demographic variables indicate high risk borrowers? This is a classification task with 30000 instances and 24 different attributes.

### Performance Metric

Accuracy

### Solution Statement

Credit card default is a serious issue that needs to be addressed. Based on the dataset, I can make the following conclusions:

- The strongest predictors of default payment is history of past payment (particularly from the most recent month) and the amount of given credit, or limit balance. Repayment status in September, 2005 had the strongest correlation to default payment next month, but all other months were correlated with default rates. Those who paid duly were least likely to default (~20%) whereas anyone who had a payment delay (regardless of how many months) had ~50-60% chance of default payment. Second, those with lower limit balance had a higher chance of default payment than people with higher limit balance.
- Some demographic populations are more prone to default. Males (~24%) were more likely to default than females (~20%). People with graduate school or other education were less likely to default than those who only studied in university or high school. In fact, those with high school diplomas had a ~25% chance of default. People with relationship status of "Other" also had a slightly higher chance of default.
-Though age didn't play a large role in default, people between ages 25-40 have a higher chance of default; however, this may be due to the fact that most credit card holders fall in that age range.

Using those conclusions, I will provide the following recommendations:
-Since there weren't any extreme demographic variables that indicated high risk borrowers, every credit card holder should receive information or a quick course on credit card usage before they are granted a card. There could also be additional information targeting the aforementioned population but it isn't necessary.
- Instead, monitoring repayment history is more useful. If any card holder fails to pay duly, monitor the holder. They could watch a video about credit card default and be required to learn more information about the issue, since those who delay payment have a higher chance of default. In addition, card holders with low credit limits should also be watched.
- The best way to predict if a cardholder is likely to default on their credit card is by applying a Random Forest algorithm.
