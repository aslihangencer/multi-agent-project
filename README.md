# 🚀 Multi-Agent Framework with Vertex AI  
### Building collaborative AI systems with Vertex AI & Gemini

---

## 🧠 Overview

I built this project to experiment with multi-agent systems using Vertex AI and Gemini.

The main idea is simple: instead of relying on a single model, multiple agents handle different parts of a task. Each agent has its own role, and they work together to produce a better final result.

Right now, the system can break down complex tasks, assign them to agents, and combine their outputs into a structured response. It’s still evolving, but it already works well for basic workflows.

---

## ❓ Why this project?

Most AI tools today follow a very straightforward pattern — input goes in, output comes out.

That works, but it often misses:
•⁠  ⁠different perspectives  
•⁠  ⁠internal validation  
•⁠  ⁠flexibility when tasks get complex  

I wanted to try a different approach.

Instead of one model doing everything, this project lets multiple agents:
•⁠  ⁠think separately  
•⁠  ⁠interact with each other  
•⁠  ⁠refine the final result together  

The goal is to move from “single response AI” → to something closer to a *collaborative system*.

---

## ✨ Key Features

•⁠  ⁠🧩 *Model-agnostic setup*  
  Works with Vertex AI, but can be adapted to other providers

•⁠  ⁠🤖 *Basic agent orchestration*  
  Tasks are split and distributed between agents

•⁠  ⁠🔄 *Agent communication*  
  Agents can exchange outputs and build on each other

•⁠  ⁠🧠 *Context handling*  
  Shared memory between agents (still improving)

•⁠  ⁠⚙️ *Modular structure*  
  Easy to add new agents or tools

•⁠  ⁠🛡️ *Output checking*  
  Some basic validation between agents

---

## 🏗️ Architecture Overview

At a high level, the system uses one orchestrator and multiple specialized agents.

```mermaid
graph TD
    User((User)) --> Orchestrator[Orchestrator Agent]
    Orchestrator --> AgentA[Research Agent]
    Orchestrator --> AgentB[Code Agent]
    AgentA <--> AgentB
    AgentA --> VertexAI[Vertex AI / Gemini]
    AgentB --> VertexAI
