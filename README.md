# Agentic-AI-for-Fair-and-Collaborative-Peer-Review
Human-in-the-Loop Agentic AI system for fair and collaborative peer review using multi-agent LLMs, trust-based voting, argumentation, and self-consistency checks. Built on the PeerRead dataset with centralized and decentralized pipelines to enhance review accuracy and fairness.

## Project Overview

Peer review remains a cornerstone of academic publishing, yet the process faces challenges of scale, bias, and inconsistency.
This project develops a Human-in-the-Loop (HITL) Agentic AI system that uses multi-agent Large Language Models (LLMs) to simulate expert review committees, fostering collaboration, fairness, and constructive reasoning in the evaluation of scientific articles.

The workflow integrates:

  1. Centralised (moderator-led) and Decentralised (peer-to-peer) orchestration.

  2. Self-consistency checks for internal review validation.

  3. Argumentation-based negotiation for deliberation among agents.

  4. Trust-based voting, where more constructive agents have higher decision weight.

  5.Human-in-the-Loop oversight, allowing approval, revision, or override of automated verdicts.


## Research Aim

To design and evaluate a Human-in-the-Loop Agentic AI that produces fair, transparent, and constructive peer-review outputs with an overall Good/Not-Good verdict, maintaining human oversight and ethical control.

## Objectives

  1. Implement multi-agent collaboration with self-consistency, negotiation, and trust-based reasoning.

  2. Compare centralised vs decentralised orchestration pipelines.

  3. Integrate a HITL decision loop for human auditing and feedback.

  4. Evaluate the system using PeerRead (arXiv cs.ai 2007-2017) dataset labels.

  5. Produce a reproducible, open-source template deployable on standard hardware.

## Research Questions

  1. Can multi-agent negotiation and trust-based voting yield more stable and fair verdicts than single LLM reviews?

  2. How do centralised and decentralised pipelines differ in accuracy, quality, and escalation frequency?

  3. Does trust weighting based on constructiveness improve decision reliability?

  4. When should human intervention occur for optimal oversight?

  5. What are common failure modes (e.g., bias, persona drift), and how can we mitigate them?

## Experimental Setup
  1. Dataset: PeerRead – arXiv cs.ai (2007–2017)
  2. Base Model: Qwen-series open-source LLM (instruction-tuned)
  3. Hardware: Viper Supercomputer (NVIDIA A40 48GB GPU)
  4. Evaluation Metrics: Accuracy, F1-score, escalation frequency, review constructiveness

## Results:
Pipeline	Accuracy	F1-Score	Observation
Centralised	0.79	0.58	More consistent, concise, stable verdicts
Decentralised	0.71	0.41	Richer debate, more HITL escalation (safer)

## System Workflow

  1. Paper ingestion from PeerRead JSON.

  2. Agentic review generation (multi-LLM roles).

  3. Self-consistency check for factual alignment.

  4. Negotiation & trust voting among agents.

  5. HITL oversight for final verdict approval.

  6. Meta-review generation and verdict output (Good / Not-Good).


## **Related Research

Jin et al. (2024) AgentReview: Exploring Peer Review Dynamics with LLM Agents

D’Arcy et al. (2024) MARG: Multi-Agent Review Generation for Scientific Papers

Ning et al. (2024) PiCO: Peer Review in LLMs based on Consistency Optimization

Bougie & Watanabe (2024) Generative Adversarial Reviews

Mudhiganti (2024) Human-in-the-Loop Agentic Systems

Permit.io (2024) Best Practices for HITL AI Agents**


## Citation

If you use this project, please cite as:

Ojei, V. (2025). Agentic AI for Fair and Collaborative Peer Review. University of Hull MSc Dissertation.
