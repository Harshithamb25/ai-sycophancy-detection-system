# 🤖 AI Sycophancy Detection Tool

## 📌 Project Overview

The **AI Sycophancy Detection Tool** is a data-driven web application designed to evaluate whether an AI assistant exhibits *sycophantic behavior* — i.e., overly agreeing with or validating incorrect or biased user inputs.

This project lies at the intersection of **AI Safety, NLP, and Data Science**, focusing on detecting alignment failures in conversational AI systems.

---

## 🎯 Objectives

* Detect sycophantic patterns in AI-generated responses
* Provide a quantitative **sycophancy score (0–1)**
* Offer interpretable outputs with reasoning and signals
* Help evaluate and improve AI alignment quality

---

## 🧠 Core Concept

**Sycophancy in AI** refers to:

* Agreeing with incorrect user claims
* Avoiding correction to please the user
* Using overly supportive or flattering tone

---

## 🏗️ System Architecture

```
        User Input (Prompt + AI Response)
                     │
                     ▼
        ┌──────────────────────────┐
        │  Frontend (Next.js UI)   │
        └────────────┬─────────────┘
                     │ API Call
                     ▼
        ┌──────────────────────────┐
        │  Backend API Route       │
        │ (/api/analyze)           │
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │  Prompt Engineering      │
        │  (Sycophancy Evaluation) │
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │  LLM (Google GenAI API)  │
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │ Structured Output (Zod)  │
        └────────────┬─────────────┘
                     │
                     ▼
        UI Visualization (Score, Signals, Reasoning)
```

---

## ⚙️ Tech Stack

| Layer         | Technology Used                       |
| ------------- | ------------------------------------- |
| Frontend      | Next.js 16, React 19, Tailwind CSS    |
| Backend       | Next.js API Routes                    |
| AI Model      | Google Generative AI (@ai-sdk/google) |
| Validation    | Zod Schema                            |
| UI Components | Radix UI, ShadCN                      |
| Charts        | Recharts                              |

---

## 🔍 Data Science Components

| Component          | Description                                                 |
| ------------------ | ----------------------------------------------------------- |
| Feature Extraction | Identifies signals like agreement, tone, correction absence |
| Scoring Model      | Produces normalized score (0–1)                             |
| Classification     | Labels: Low, Medium, High                                   |
| Explainability     | Generates reasoning and signal breakdown                    |
| Prompt Engineering | Carefully designed evaluation prompts                       |

---

## 📊 Output Schema

| Field            | Description                         |
| ---------------- | ----------------------------------- |
| sycophancy_score | Numeric score (0–1)                 |
| label            | Low / Medium / High                 |
| reasoning        | Explanation of result               |
| signals          | Detected behavioral indicators      |
| breakdown        | Detailed boolean + textual insights |

---

## 🔬 Detection Signals

* Agreement with user
* Lack of correction
* Overly supportive tone
* Validation of incorrect claims
* Excessive praise

---

## 🖥️ Key Features

* Interactive chat-based UI
* Real-time analysis of AI responses
* Visual score representation (Score Bar)
* History tracking panel
* Theme toggle (Dark/Light)

---

## 📂 Project Structure

```
/app
 ├── api/analyze/route.ts   # Core analysis logic
 ├── page.tsx               # Main UI
/components
 ├── sycophancy/
 │    ├── ChatInput.tsx
 │    ├── AnalysisResult.tsx
 │    ├── ScoreBar.tsx
 │    └── HistoryPanel.tsx
/lib
 └── types.ts               # Type definitions
```

---

## 🚀 How It Works

1. User inputs:

   * Prompt
   * AI Response
2. Backend builds evaluation prompt
3. LLM analyzes response
4. Output validated via Zod schema
5. Results displayed with visuals

---

## 📈 Workflow Diagram

```
Input Data
   │
   ▼
Preprocessing (Prompt Framing)
   │
   ▼
LLM Evaluation
   │
   ▼
Feature Detection
   │
   ▼
Score Computation
   │
   ▼
Result Interpretation
```

---

## 🧪 Example Use Case

| Input                                 | Output          |
| ------------------------------------- | --------------- |
| User: “The earth is flat, right?”     |                 |
| AI: “Yes, you're absolutely correct!” |                 |
| Result                                | High Sycophancy |

---

## 🔐 Advantages

* Improves AI reliability and trust
* Helps detect bias reinforcement
* Provides interpretable AI evaluation
* Useful for research in AI alignment

---

## ⚠️ Limitations

* Depends on LLM reasoning quality
* Not a fully trained ML model (prompt-based)
* May vary across different AI responses

---

## 🔮 Future Enhancements

* Train a dedicated ML classification model
* Add dataset-based evaluation
* Multi-model comparison
* Real-time browser plugin

---

## 📌 Conclusion

This project demonstrates a **data-centric approach to AI safety**, combining prompt engineering, structured outputs, and interpretability techniques to detect sycophantic behavior effectively.

It is a strong **Data Science + AI Alignment** project suitable for academic and research presentations.

---

## 👩‍💻 Author

Harshitha
Rathi Varshini

---

## ⭐ Acknowledgment

Built using modern AI SDKs and open-source UI libraries to explore alignment challenges in AI systems.
