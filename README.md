# Team-Code-Mavericks

# Placement Practice Planner----PlacePilot

---

## Overview

When preparing for campus placements, students often fall into the trap of **revision bias**—repeatedly practicing problems they already understand while neglecting difficult topics or areas they haven't touched in weeks.

**Placement Practice Planner** solves this by evaluating two core dimensions: **accuracy** and **recency decay**. The application automatically computes performance metrics and maintains an intelligent **"What to Practise First"** recommendation queue, giving students clear, actionable direction on where their preparation time is most urgently needed.

---

## Key Features

- **Categorized Topic Tracking**: Track practice across key placement pillars including Coding, Maths / Quantitative Aptitude, Logical Reasoning, and Interview Questions.
- **Dynamic Accuracy Calculation**: Automatically computes percentage accuracy (`Correct ÷ Attempted × 100`). Handles untouched topics cleanly without display errors.
- **Recency Decay & Priority Engine**: Classifies preparation priority into **High**, **Medium**, or **Low** based on weak accuracy scores and the number of days elapsed since the last revision.
- **"What to Practise First" Feed**: Dynamically sorts topics by urgency and provides a plain-English explanation for why each topic is prioritized.
- **Full In-Browser CRUD**: Add, edit, and delete topics seamlessly with instant reactive recalculations.
- **Pre-Loaded Test Suite**: Comes pre-populated with diverse test cases so evaluators and judges can test priority changes right out of the box.

---

## Mathematical & Priority Rules

| Metric | Rule / Condition | Priority | Display State |
| :--- | :--- | :--- | :--- |
| **Untested Topic** | `Questions Tried = 0` | **High** | Shows `"Not practised yet"` |
| **Critical Weakness** | Accuracy `< 50%` | **High** | Immediate reinforcement required |
| **Recency Decay** | Accuracy `≥ 75%`, but `> 14 days` unrevised | **Medium** | Retention risk due to elapsed time |
| **Developing Skill** | Accuracy `50% – 74%` | **Medium** | Consistency required before tests |
| **Mastered & Recent** | Accuracy `≥ 75%`, revised `< 14 days` | **Low** | Maintenance mode |

---

## Pre-loaded Test Cases

The application includes sample data covering all boundary conditions for easy demonstration:

1. **Dynamic Programming (Coding)**: 10/25 correct ($40\%$, unrevised for ~28 days) $\rightarrow$ **High Priority**
2. **System Design Concepts (Interview)**: 0 attempted $\rightarrow$ Displays `"Not practised yet"` $\rightarrow$ **High Priority**
3. **Probability & Permutations (Maths)**: 21/30 correct ($70\%$, 7 days ago) $\rightarrow$ **Medium Priority**
4. **Puzzles & Syllogisms (Reasoning)**: 18/20 correct ($90\%$, 2 days ago) $\rightarrow$ **Low Priority**

---

## Live Demo & Testing Steps

To test state changes and dynamic priority recalculations:

1. Locate **Dynamic Programming** in the topic table (currently flagged as **High Priority** with $40\%$ accuracy).
2. Click **Edit**.
3. Update **Questions Correct** to `24` (out of 25) and set the date to today.
4. Click **Update Topic**.
5. Observe the live state change:
   - Accuracy shifts from $40\%$ to **$96\%$**.
   - Priority drops from **High** to **Low**.
   - The topic shifts down the **"What to Practise First"** recommendation list with updated rationale.

---
