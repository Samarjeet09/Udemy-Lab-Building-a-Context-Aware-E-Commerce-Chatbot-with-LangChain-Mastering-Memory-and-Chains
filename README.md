# Context-Aware E-Commerce Chatbot with LangChain
*A Udemy Lab Project*

## Overview
This repository contains the implementation of a **context-aware, multi-step, and memory-enabled e-commerce chatbot** built using [LangChain](https://python.langchain.com/).

The chatbot is designed to handle real-world customer service scenarios such as:
- Order tracking
- Product inquiries
- Return and refund processing
- Multi-turn, context-aware conversations
- Complex workflows requiring multiple processing steps

**Key Goal:** Build a **production-ready prototype** that delivers seamless customer support, improves response times, and ensures customers don’t have to repeat themselves.

---

## Lab Scenario
Customers in an e-commerce setting often:
- Switch topics mid-conversation (e.g., from product inquiry → order status → return request)
- Engage in **multi-turn dialogues** where context must be retained
- Ask complex questions that require multi-step processing

This lab demonstrates how to use **LangChain’s Chains, Memory modules, and Sequential workflows** to create a chatbot that:
- **Remembers context** across interactions
- **Summarizes long conversations** to manage token limits
- **Executes multi-step processes** in an ordered and logical manner

---

## Tasks Breakdown

### Task 1 – Building a Basic E-Commerce Chatbot with `LLMChain`
- **Goal:** Handle single-step queries like order status, product details, and refund policy.
- **What you’ll do:**
  - Create **PromptTemplates** to standardize responses
  - Use `LLMChain` for processing user inputs
  - Test chatbot for various scenarios
- **Key Docs:**
  - [LangChain LLMChain Documentation](https://python.langchain.com/docs/modules/chains/llm_chain)
  - [Prompt Templates](https://python.langchain.com/docs/modules/model_io/prompts/prompt_templates)

---

### Task 2 – Enhancing Conversations with `ConversationBufferMemory`
- **Goal:** Enable chatbot to remember previous turns in a conversation.
- **What you’ll do:**
  - Initialize `ConversationBufferMemory`
  - Integrate with `ConversationChain`
  - Retrieve and inspect stored history
- **Key Docs:**
  - [ConversationBufferMemory](https://python.langchain.com/docs/modules/memory/types/buffer)
  - [ConversationChain](https://python.langchain.com/docs/modules/chains/popular/conversation_chain)

---

### Task 3 – Managing Long Conversations with `ConversationSummaryBufferMemory`
- **Goal:** Keep essential context without exceeding token limits.
- **What you’ll do:**
  - Use summaries instead of full transcripts
  - Efficiently handle multi-topic, long-running conversations
- **Key Docs:**
  - [ConversationSummaryBufferMemory](https://python.langchain.com/docs/modules/memory/types/summary_buffer)

---

### Task 4 – Creating Multi-Step Workflows with `SequentialChain`
- **Goal:** Execute multiple logical steps for complex requests.
- **What you’ll do:**
  - Build individual chains (e.g., order verification → return processing → refund estimate)
  - Combine them into a **SequentialChain** for structured execution
- **Key Docs:**
  - [SequentialChain Documentation](https://python.langchain.com/docs/modules/chains/foundational/sequential_chains)

---

### Task 5 – Combining Memory + Chains for a Context-Aware Multi-Step Chatbot
- **Goal:** Create a chatbot that can:
  - Remember multiple topics across a conversation
  - Execute multi-step processes
  - Switch between intents naturally
- **What you’ll do:**
  - Combine `SequentialChain` with `ConversationSummaryBufferMemory`
  - Enable topic-switching without losing context
- **Key Docs:**
  - [LangChain Memory Overview](https://python.langchain.com/docs/modules/memory)
  - [Combining Chains & Memory](https://python.langchain.com/docs/guides/chains/combining)

---