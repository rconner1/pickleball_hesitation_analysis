# The Cost of Indecision: Analyzing Hesitation in Pickleball Rallies

## Overview

This project investigates whether visible player hesitation during doubles pickleball rallies is associated with rally outcomes and the type of error that ends a point.

I manually coded 200 rallies from publicly available Major League Pickleball match footage. Each row represents one rally and includes information on serving team, receiving team, shots, hesitation, error type, and rally outcome.

## Research Questions

1. Is player hesitation associated with the serving team's probability of winning a rally?
2. Are certain error types associated with worse rally outcomes?
3. Does server hesitation relate to the type of error that ends a rally?

## Key Findings

- When the serving team did not hesitate, it won 62.7% of rallies. When the serving team hesitated, it won 22.2% of rallies.
- Logistic regression estimated that server hesitation was associated with a 39.8 percentage point decrease in predicted serving-team win probability.
- Receiver hesitation was associated with a 20.1 percentage point increase in predicted serving-team win probability.
- Decision errors were associated with the lowest serving-team win rate at 16.7%, compared with 54.1% for execution errors and 46.9% for positional errors.
- Decision errors occurred in longer rallies on average and were more common when the serving team hesitated.

## Data

The dataset contains 200 manually coded doubles rallies from Major League Pickleball matches.

Each observation is one rally. Variables include:

- Game ID and rally ID
- Serving and receiving team
- Total shots and shots by each team
- Server and receiver hesitation indicators
- Number of hesitations
- Error type: positional, decision, or execution
- Rally outcome: whether the serving team won the point

Hesitation was coded when a player visibly paused before moving, stopped moving forward after a playable shot, drifted backward under non-extreme pressure, or showed uncertainty with a partner about who should take the ball.

## Methods

- Exploratory data analysis and visualization
- Logistic regression predicting serving-team rally wins
- Chi-square tests of association
- Pairwise two-proportion z-tests with Bonferroni correction
- One-way ANOVA comparing rally length across error types
- Hesitation Impact Score, a custom metric combining the effects of server and receiver hesitation on rally outcomes

## Tools

- R
- R Markdown
- tidyverse
- ggplot2
- Logistic regression
- Statistical inference

## Limitations

This is an observational study using a modest manually coded sample. Hesitation labels can involve subjective judgment, and the analysis does not account for potential confounders such as player skill, score, fatigue, opponent strength, or shot location.

The findings describe associations and should not be interpreted as causal effects.

