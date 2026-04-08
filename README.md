# agentic-admet-predictor
Agentic ADMET Predictor: RDKit + LLM agent for drug-likeness triage & biological reasoning

## Overview
Drug discovery often fails due to poor ADMET properties (Absorption, Distribution, Metabolism, Excretion, Toxicity). Traditional rule-based filters (e.g., Lipinski) are useful but lack contextual reasoning.
This agentic pipeline computes RDKit descriptors, then Gemini reasons biologically, and suggests optimizations.

## Key Features
- **RDKit Engine:** 10 core ADMET descriptors (MW, logP, TPSA, etc.)
- **Gemini Agent:** Biological interpretation and optimization
- **Agentic Loop:** Plan (Evaluate) → Act (Compute) → Reflect (Reason) → Improve (Optimize)  
- **Validation:** 4-steps, lookling at baseline (Aspirin, Ibuprofen), tradeoff (Metformin, Lopinavir), non-drug-like/failure molecules (sucrose, stearic acid) and real-world drugs (Chloroquine, Imatinib)

**Skills:** Structured LLM prompting, tool integration, biological hypothesis generation

## Results
Graph of Results
<img width="990" height="690" alt="agentic-admet-results" src="https://github.com/user-attachments/assets/2317c11a-bf86-4f8f-8143-832b9127dc57" />

Table of Results
<img width="900" height="390" alt="agentic-admet-results-table" src="https://github.com/user-attachments/assets/029c6296-d502-4736-83ee-8a4bd809447f" />
See `output/` for full tables and agent reasoning.





