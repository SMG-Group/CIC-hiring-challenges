# 🚀 Data/ML Engineer Challenge

## 👋 Introduction

This challenge is designed to evaluate your ability to implement a small **Python-based backend service** along with a **data processing script**. 
Your solution should demonstrate clean and maintainable code, while prioritizing **readability**, **simplicity**, and **clear thinking**.

---

##  Goal of this challenge

The goal is to prepare and normalize listing data from different online property platforms as a preprocessing step for finding matches across platforms.
All platforms have different formats and data types, the goal is to unify the data into a common format.

## 📦 Task Overview

Your goal is to build a simple data normalization pipeline consisting of two parts:

1. A **Processor** script that reads input data and sends it to a backend service.
2. A **Service** that exposes a REST API and returns normalized records.

You're free to use any Python libraries or tools that help you achieve this, but please make your choices with care and document your decisions.

---

## 📂 Dataset

The dataset you'll be working with is available on Google Drive:  
👉 [Download the file here](<https://drive.google.com/file/d/1Yex5VDiyVVGAC5GpwEbrPFXxtzfHLmfp/view?usp=drive_link>)

This file contains raw data that you’ll be normalizing in your solution. Each line in the file represents a real-estate listing JSON object.

---

## 🧩 Task Breakdown

### 1. 🔄 Processor

Implement a Python script that:
- On trigger (manual run or cron), reads the input file.
- Sends the data (one or more records) to the backend normalization service.
- Receives a normalized response from the service.
- Writes the normalized output to a file (this output is the final result of the challenge).

This can be implemented as a simple script or CLI tool.

---

### 2. 🌐 Service

Build a **REST API** that accepts one or more JSON records via `POST`. Then it:
- Performs **Normalization**:
  - Normalize the following fields: `price`, `floor`, `living_space`, `propertyCategory` (apartment, house, ground, commercial, other), `title`, `street`. Focus on transforming data into consistent formats suitable for both backfilling to and SMG platform (prio 1) as well as ML (prio 2) (e.g., numerical scaling, categorical encoding strategies, text cleaning).
  - Crucially, reflect on and document any assumptions or strategies for handling potential outliers or missing values encountered in these fields.
- Performs **Feature Engineering**:
  - Based on the available fields in the raw data, identify and implement the calculation of at least **1-2 new features** you believe would be valuable for an ML-based property matching model. Examples could e.g. include price per square meter, text length features.
  - Be ready to explain why you chose these features in your documentation.
- Returns the processed records in the response, including both the normalized original fields and the newly engineered features.

Please focus on normalizing the following fields:
- `price`
- `floor`
- `living_space`
- `propertyCategory` - (apartment, house, ground, commercial and other)
- `title`
- `street`

---

If you believe other fields should be normalized, feel free to include them, or mention how/why you would include them. Explain your reasoning in the documentation.

In addition to documenting your setup, assumptions, and code structure, please include a dedicated **DATA ANALYSIS** section in your README documentation, addressing the following ML-related points:

#### Data Analysis & Handling:
- Briefly describe the characteristics of the key input fields (e.g., distributions, presence of outliers, missing data).
- Detail your strategy for handling outliers and missing values during normalization, considering the potential impact on a downstream matching task.

#### Feature Engineering:
- Explain the rationale for the specific feature(s) you engineered. Why are they potentially useful for matching?

#### ML Matching Strategy:
- **Other Crucial Fields:** What other data fields (beyond those in the provided dataset, assuming a typical property listing) do you think are most crucial for building a highly effective ML-based matching model, and why?
- **Proposed ML Approach:** Briefly outline one or two ML approaches you would consider for the matching task itself. 

---

## 🛠 Project Guidelines

- Be pragmatic because this is the test assignment, but be prepared to explain how would you scale and make changes for production environment
- Include a `Dockerfile` to build the project
- Provide a `docker-compose.yml` file for local testing (optional but nice to have)
- Document any assumptions, TODOs, and decisions in this README or a separate doc
- We advise you to work **6–8 hours** on this. If you can’t finish, include notes on how you would proceed.

---

## 🧪 Evaluation Criteria

We're looking for:

- Ability to break down business requirements into working code
- The project builds and runs with one command
- Clean code and sound architecture
- **Quality of data analysis and strategy for handling outliers/missing data**
- **Clarity, feasibility, and depth of thought in the DOCUMENTATION and DATA ANALYSIS section**
- Proper use of framework and language idioms
- Smart usage of external libraries and tools
- Reasonable trade-offs and decision-making
- Well-documented code and reasoning

---

## 🎁 Bonus Points

- Add extra features, clever touches, or even fun easter eggs
- Extra bonus points for making us laugh 😄

---

## 💡 Hints

- Double-check that your final commit compiles and runs
- Submit a link to your code repo (e.g. GitHub)

---

Thanks and good luck! 🚀
