# FIFA World Cup 2026 Prediction Analysis

## 1. Project Overview

This project develops a data-driven model to identify the strongest contenders for the FIFA World Cup 2026.

A custom **Team Strength Score** was created by combining historical performance, recent form, FIFA rankings, and squad market value. The model was then used to simulate the official FIFA World Cup 2026 tournament and predict the most likely champion.

---

## 2. Project Objective

The main objective is to estimate which national teams have the highest probability of reaching the final stages of the FIFA World Cup 2026 using publicly available football data.

Key goals:

* Build a Team Strength Score model.
* Rank the 48 qualified teams.
* Visualize the results using Tableau.
* Simulate the official FIFA World Cup 2026 tournament.
* Predict the champion, runner-up, and semifinalists.

---

## 3. Data Sources

### International Football Results (1872–2026)

Used to calculate:

* Recent Performance Score
* World Cup History Score

### FIFA Rankings

Used to calculate:

* FIFA Ranking Score

### Transfermarkt National Team Market Values

Used to calculate:

* Squad Value Score

---

## 4. Team Strength Score Methodology

The final score combines four indicators:

| Indicator                | Weight |
| ------------------------ | ------ |
| Recent Performance Score | 35%    |
| FIFA Ranking Score       | 35%    |
| World Cup History Score  | 20%    |
| Squad Value Score        | 10%    |

### Formula

Team Strength Score =
0.35 × Recent Performance Score +
0.35 × FIFA Ranking Score +
0.20 × World Cup History Score +
0.10 × Squad Value Score

All variables were normalized to a 0–100 scale before weighting.

---

## 5. Top 10 Teams Ranking

| Rank | Team        | Score |
| ---- | ----------- | ----- |
| 1    | Spain       | 90.77 |
| 2    | France      | 89.30 |
| 3    | Argentina   | 87.66 |
| 4    | England     | 83.01 |
| 5    | Germany     | 78.96 |
| 6    | Morocco     | 77.37 |
| 7    | Netherlands | 75.52 |
| 8    | Portugal    | 75.49 |
| 9    | Brazil      | 70.92 |
| 10   | Senegal     | 67.34 |

---

## 6. Tableau Dashboard

The project includes an interactive Tableau dashboard containing:

### Top 10 Teams Ranking

Visual comparison of the strongest national teams.

### History vs Current Form

Scatter plot comparing World Cup history and recent performance.

### Team Strength Components

Breakdown of the four variables contributing to the final score.

## Tableau Dashboard

![Tableau Dashboard](visuals/tableau_dashboard.png)

---

## 7. Tournament Simulation

The official FIFA World Cup 2026 groups and knockout bracket were used to simulate the tournament.

### Group Stage

* Teams were ranked according to Team Strength Score.
* Top two teams from each group advanced.
* Eight best third-place teams advanced to the Round of 32.

### Knockout Stage

A deterministic approach was used:

Winner = Team with the highest Team Strength Score

The simulation covered:

* Round of 32
* Round of 16
* Quarterfinals
* Semifinals
* Final

---

## 8. Predicted Knockout Bracket

## Tournament Simulation

![World Cup Bracket](visuals/world_cup_2026_bracket.png)

---

## 9. Predicted Results

### Champion

🏆 Spain

### Runner-Up

🥈 Argentina

### Semifinalists

* Spain
* Argentina
* France
* England

---

## 10. Limitations

This simulation is deterministic and assumes that the team with the highest Team Strength Score always wins.

The model does not account for:

* Injuries
* Tactical decisions
* Penalty shootouts
* Home advantage
* Random match events

Therefore, results should be interpreted as analytical estimates rather than exact predictions.

---

## 11. Future Improvements

Potential future enhancements include:

* Monte Carlo tournament simulations
* Probability-based match predictions
* Elo rating integration
* Expected Goals (xG) metrics
* Player-level performance indicators

---

## Tools Used

* Python
* Pandas
* Excel
* Tableau Public
* GitHub
