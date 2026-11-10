# Measuring Product Speculation on Steam

**Warwick Business School doctoral research**

## Research Question

Do the things players speculate about before a game launches tell us more about sales and reviews than the amount and tone of pre-release discussion alone?

## Data and Modelling

- **Data engineering:** Matched Steam discussion and product data to sales estimates, search trends and news coverage. Aligned records to each game's release date. The discussion corpus contains **7.96 million posts and comments across 1,695 games**.
- **Applied NLP:** Fine-tuned DistilRoBERTa models to identify speculation and uncertainty cues, and used BERTopic to group posts by product topic. Checked the resulting classifications against **500 independently annotated sentences**.
- **Statistical modelling:** Used regression to estimate associations with sales, revenue and reviews. Evaluated predictions on games from publishers held out of training to avoid sharing publisher information between the training and evaluation sets.

One speculation measure improved sales and revenue predictions compared with models using standard buzz metrics. The analysis shows predictive value, not that speculation caused higher sales.

## Public Evidence

- [Sentence validation exercise](https://github.com/daakrofi/prus-human-validation-sentence-components): The annotation rubric, browser interface and blinded 500-sentence sample. It does not include model predictions or annotator responses.
- [Steam data collection utility](https://github.com/daakrofi/Steam-Data-Collection): A Python utility that generates paginated discussion URLs from Steam app IDs. This is one part of the collection workflow, not the entire research pipeline.

The full discussion corpus and trained models are not included in these repositories.

## Ongoing Study

A follow-up paper examines how official pre-release announcements shift uncertainty in Steam discussions. The design uses a local-projections difference-in-differences event study and Bayesian structural time-series models, comparing matched games at the same stage before release.
