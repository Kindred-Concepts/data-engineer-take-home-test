
# Data Engineer Take-Home Assignment

## Overview

This take-home assignment is designed to evaluate your ability to work with large-scale data processing, optimize ETL pipelines, and distributed systems like PySpark or Spark.

---

## Dataset Description

You are provided with three CSV files:

### 1. `users.csv`

| Column Name          | Type    |
|----------------------|---------|
| id                   | String  |
| home_destination_id  | String  |

### 2. `travel_plans.csv`

| Column Name   | Type    |
|---------------|---------|
| id            | String  |
| user_id       | String  |
| created_at    | Date    |
| destination_id| String  |

### 3. `trip_matching.csv`

| Column Name     | Type    |
|------------------|---------|
| id               | String  |
| travel_plan_id   | String  |
| start_date       | Date    |
| end_date         | Date    |
| home_id          | String  |

---

## Task 1: Long-Duration Matches

**Goal**: Find users whose **average match duration** is **greater than 7 days**.

1. Write code to join the necessary tables and compute the average match duration per user.
2. Return the list of user IDs that meet this criterion.
3. **Follow-up**: Assume `users` and `travel_plans` are small (≈10K records), but `trip_matching` is large (≈1B records). List **at least two ways** to optimize your solution. If the full solution is too complex to write in under 100 lines of code, please provide pseudocode or outline concrete optimization approaches.

---

## Task 2: Match Density

**Goal**: Calculate the **average number of matches per travel plan**.

1. Write code that outputs the average number of matches for all travel plans.
2. **Follow-up**: If both `travel_plans` and `trip_matching` tables are very large, explain how to **efficiently join** these tables. Mention any join strategies or optimizations you would apply. If the full solution is too complex to write in under 100 lines of code, please provide pseudocode or outline concrete optimization approaches.

---

## Submission

- Submit your code as `.py`, jar package, or `.ipynb` files.
- Provide a short write-up explaining your optimization approaches.
