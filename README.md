# ThinkPalm AgentAI - Lab 2: SMS Delivery Service BDD & Playwright Automation

* **Name:** Babu
* **Track:** AgentAI / Quality Engineering
* **Lab Name:** SMS Delivery Service Test Automation

## What It Does
This project automates and validates BDD-style test scenarios for a telecom SMS gateway. It utilizes Playwright's network route interception (`page.route`) to mock backend API behaviors dynamically—testing successful deliveries (200), invalid recipients (400), payload boundary limits $>160$ chars (422), gateway server outages (503), and automatic transient failure retry logic (503 $\rightarrow$ 200).

## How to Run
1. Open the notebook inside `src/` using Google Colab.
2. Install dependencies: `!pip install playwright && playwright install --with-deps`
3. Run all cells sequentially. Execution logs and evidence screenshots will be generated automatically.

## Observations
* Mocking network routes via Playwright ensures fast, deterministic testing without hitting external live telecom APIs.
* Client-side retry loops successfully handle transient network drops, recovering automatically on the second attempt.
