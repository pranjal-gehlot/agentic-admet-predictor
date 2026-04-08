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
The agentic ADMET workflow excels across validation scenarios, correctly identifying Aspirin/Ibuprofen (100.0 scores) as ideal oral drugs while crushing Lopinavir and Sucrose for realistic liabilities—peptide-like flexibility and poor permeability, respectively. Metformin's nuanced 83.7 score despite logP=-0.56 demonstrates sophisticated polarity tradeoffs, and Imatinib's 77.6 (despite Lipinski failure) reflects kinase inhibitor realities. The Gemini agent's biological reasoning consistently aligns with medicinal chemistry intuition.
See `output/` for full tables and agent reasoning.

## Quick Start
See 'notebook/' for the notebook and code







