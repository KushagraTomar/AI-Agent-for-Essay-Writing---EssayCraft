# AI-Agent-for-Essay-Writing---EssayCraft

# 📝 EssayCraft: LangGraph Agent for Essay Writing

![image](https://github.com/user-attachments/assets/049b06b0-dc4e-4447-a7ae-0cf8739da8ed)

## 📌 Overview

**EssayCraft** is an autonomous essay-writing agent built using [LangGraph](https://github.com/langchain-ai/langgraph) and powered by **Meta's LLaMA 3.1-8B-Instruct** model. This agent is designed to assist users in crafting structured, high-quality essays with iterative improvement based on research, critique, and reflection.

The agent flows through multiple intelligent stages including planning, research, writing, and feedback — all orchestrated using a stateful LangGraph workflow.

---

## 🧠 Architecture

The agent comprises the following key nodes:

### 1. `planner`
**Purpose**: Creates a high-level outline for the essay.

**Prompt Summary**:
- Identifies the thesis or core idea.
- Structures the essay into Introduction, Body Paragraphs, and Conclusion.
- Provides tips, stylistic suggestions, and flow guidance.

### 2. `research_plan`
**Purpose**: Suggests up to three targeted search queries for background research.

**Prompt Summary**:
- Focuses on finding credible facts, arguments, expert opinions, or historical context.
- Aims to enrich the content before writing begins.

### 3. `generate`
**Purpose**: Generates the full 5-paragraph essay.

**Prompt Summary**:
- Follows classic essay structure: Introduction, 3 Body Paragraphs, Conclusion.
- Ensures coherence, flow, and stylistic accuracy.
- Uses planner and research outputs for writing guidance.

### 4. `reflect`
**Purpose**: Reviews the essay and provides constructive feedback.

**Prompt Summary**:
- Highlights strengths and areas for improvement.
- Offers suggestions on tone, clarity, style, and depth.
- Mimics feedback from a professional writing coach.

### 5. `research_critique`
**Purpose**: Refines research queries based on critique feedback.

**Prompt Summary**:
- Suggests improved queries to address content gaps or weaknesses.
- Helps strengthen revised drafts with better evidence and examples.

![image](https://github.com/user-attachments/assets/be14aa4d-4119-48d7-80fc-63093e8e56a6)


---

## 🔁 Flow Description

1. **Start** ➝ `planner` ➝ `research_plan` ➝ `generate`
2. Essay is optionally routed to:
   - `reflect` ➝ `research_critique` ➝ back to `generate` for iteration
   - or directly to **End**

This cyclical flow allows the essay to be improved iteratively based on critique and refined research.

---

## 🚀 Technologies Used

- 🧠 Meta LLaMA 3.1-8B-Instruct
- 🔗 LangGraph
- 🧱 LangChain
- 🐍 Python

---

## 💡 Getting Started

1. **Clone the repository**

```
git clone https://github.com/yourusername/essaycraft-langgraph.git
cd essaycraft-langgraph
```

## 📈 Future Improvements

- Integration with real-time search APIs (e.g., SerpAPI)
- Web UI for user input and essay rendering
- Support for different writing formats (e.g., argumentative, narrative, expository)

## 🧑‍🎓 Ideal Use Cases

- Students drafting academic essays
- Professionals crafting blog posts or opinion pieces
- Educators looking to teach writing through AI-assisted feedback

## 🧑‍🎓 Ideal Use Cases

- Students drafting academic essays
- Professionals crafting blog posts or opinion pieces
- Educators looking to teach writing through AI-assisted feedback

## 📄 License

This project is licensed under the MIT License.

