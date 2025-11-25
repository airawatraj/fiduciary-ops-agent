# 🛡️ Fiduciary Agent: The Risk-Aware Orchestrator

## 1. The Pitch
**The Problem:**
Most AI agents are "Yes-Men", they prioritise politeness over business rules. In e-commerce, an agent that approves every refund request can bankrupt a company. Simple chatbots lack the context to distinguish between a VIP customer and a fraudulent claim.

**The Solution:**
The **Fiduciary Agent**. This is not a chatbot; it is an **Authorised RPA Controller**. It acts with "Fiduciary Responsibility," calculating **Customer Lifetime Value (CLV)** and assessing risk *before* executing any financial transaction. It empowers `Gemini-Flash-Lite` to say "No" when necessary, protecting the enterprise bottom line.

## 2. Architecture: Brain, Hands, & Memory
The system moves beyond simple conversation to a strict **"Check-then-Act" Protocol**:

* **🧠 The Brain (Gemini 2.5 Flash Lite):** Acts as the "Controller." It does not make up answers; it strictly follows a sequence to invoke the correct tools.
* **🦾 The Hands (Custom Tools):** Python-based governance layer. The business logic (Math, Risk Ratios, Bank Balances) is hidden here. The tool *physically blocks* the agent from processing risky refunds.
* **💾 The Memory (Session Service):** Maintains the user's identity (`judge_01`) and context across turns, allowing the agent to handle multiple requests in a single session without amnesia.

![Fiduciary AI Agent - The Risk Aware Orchestrator Architecture](https://github.com/airawatraj/fiduciary-ops-agent/blob/main/assets/Fiduciary-AI-Agent-TheRisk-Aware-Orchestrator-Architecture.png)

## 3. Course Concepts Demonstrated
This submission explicitly implements three core concepts from the **5-Day AI Agents Intensive Course with Google**:

1.  **Agent Powered by an LLM:** Leveraging `gemini-2.5-flash-lite` for high-speed, low-latency reasoning.
2.  **Custom Tools:** Implementation of `execute_refund` which returns rich objects (Status + CLV + Risk Flag), not just text strings.
3.  **Sessions & State Management:** Using `InMemorySessionService` to persist the conversation state and user identity.

## 4. Setup
* **Framework:** Google Agent Development Kit (`ADK`)
* **Model:** `gemini-2.5-flash-lite` (Optimised for Edge/Speed)
* **Logic:** Enterprise Risk Governance (`CLV > Refund Value`)
