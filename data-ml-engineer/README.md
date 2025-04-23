# 🚀 Data/ML Engineer Challenge

## 👋 Introduction

This challenge is designed to evaluate your ability to implement a small **Python-based backend service** along with a **data processing script**. Your solution should demonstrate clean and maintainable code, while prioritizing **readability**, **simplicity**, and **clear thinking**.

---

## 📦 Task Overview

Your goal is to build a simple data normalization pipeline consisting of two parts:

1. A **Processor** script that reads input data and sends it to a backend service.
2. A **Service** that exposes a REST API and returns normalized records.

You're free to use any Python libraries or tools that help you achieve this, but please make your choices with care and document your decisions.

---

## 📂 Dataset

The dataset you'll be working with is available on Google Drive:  
👉 [Download the file here](<link>)

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

Build a **REST API** that:
- Accepts one or more JSON records via `POST`.
- Returns normalized records in the response.

Focus on normalizing the following fields:
- `price`
- `floor`
- `rooms`
- `living_space`
- `propertyCategory`

If you believe other fields should be normalized, feel free to include them. Explain your reasoning in the documentation.

You can use external libraries or a database if needed — just document your choices.

---

## 🛠 Project Guidelines

- Include a `Dockerfile` to build the project
- Provide a `docker-compose.yml` file for local testing (optional but nice to have)
- Document any assumptions, TODOs, and decisions in this README or a separate doc
- You have **5–8 hours** to work on this. If you can’t finish, include notes on how you would proceed.

---

## 🧪 Evaluation Criteria

We’re looking for:

- Ability to break down business requirements into working code
- The project builds and runs with one command
- Clean code and sound architecture
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
