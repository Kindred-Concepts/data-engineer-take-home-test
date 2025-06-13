
# Data Engineer Take-Home Assignment

## Overview

This take-home assignment is designed to evaluate your ability to work with large-scale data processing, optimize ETL pipelines, and work with distributed systems like PySpark or Spark.

---

## Dataset Description

You are provided with three CSV files:

### 1. `users.csv`

| Column Name          | Type    |
|----------------------|---------|
| id                   | String  |

### 2. `user_engagement_survey.csv`

| Column Name   | Type    |
|---------------|---------|
| id            | String  |
| user_id       | String  |
| created_at    | Date    |
| question_id   | String  |

### 3. `engagement_answer.csv`

| Column Name   | Type    |
|---------------|---------|
| id            | String  |
| survey_id     | String  |
| question_id   | String  |
| answer        | String  |

---

## Task 1: Highly Engaged Users

**Goal**: Identify users who have answered **more than 7 questions**.

1. Join `user_engagement_survey` and `engagement_answer` on `survey_id`.
2. Count the number of **distinct question_id** values answered per user.
3. Return the list of **user IDs** who have answered more than 7 questions.
4. **Follow-up**: Assume `users` and `user_engagement_survey` are small (≈10K records), but `engagement_answer` is large (≈1B records). Describe at least two strategies to optimize this computation (e.g., broadcast joins, partitioning, etc.).

---

## Task 2: Survey Density

**Goal**: Calculate the **average number of answers per engagement survey**.

1. Write code that outputs the average number of answers per `survey_id`.
2. **Follow-up**: If both `user_engagement_survey` and `engagement_answer` are large datasets, explain how to **efficiently join** these tables. Mention any join strategies or optimizations you would apply (e.g., shuffling, filtering early, column pruning, etc.). If the full solution is too complex to write in under 100 lines of code, you may provide pseudocode or outline concrete optimization approaches.

---

## Submission

- Submit your code as `.py`, `.jar`, or `.ipynb` files.
- Provide a short write-up explaining your optimization techniques.
