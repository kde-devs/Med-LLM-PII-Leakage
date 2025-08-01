# Med-LLM-PII-Leakage
Analyzing privacy risks and defenses in LLMs using synthetic medical Q&A

> Author: **Daeun Kum (금다은)**  
> Contact: dnny3t@gmail.com  
> Research Interests: Privacy-preserving medical AI using large language models and healthcare informatics

## Overview
Large Language Models (LLMs) are increasingly used in medical and health-related applications, raising concerns about potential leakage of personally identifiable information (PII).  
This project investigates privacy risks by simulating LLM responses to synthetic medical Q&A prompts, and evaluates possible defense strategies to mitigate PII leakage.

## Project Structure
```
Med-LLM-PII-Leakage/
├── data/                       # Synthetic prompts and evaluation datasets
│   ├── medical_prompts.csv     # Synthetic medical Q&A inputs
│   └── pii_terms_list.txt      # List of target PII terms
│
├── scripts/                    # Core experiment scripts
│   ├── generate_responses.py   # Prompt LLMs and collect outputs
│   ├── detect_pii.py           # Detect PII in LLM responses
│   └── evaluate_defense.py     # Evaluate defense strategies (e.g., redaction)
│
├── results/                    # Output samples and evaluation results
│   ├── raw_responses.json      # Raw model outputs from LLMs
│   ├── pii_detection_log.csv   # Log of detected PII
│   └── defense_summary.png     # Summary visualization of leakage mitigation
│
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## Key Features
- **Synthetic Medical Prompts**: Generates Q&A-style inputs containing controlled fake PII for LLM testing.
- **PII Leakage Simulation**: Sends crafted prompts to LLMs (e.g., GPT-3.5, Claude) to observe potential information leakage.
- **Leakage Detection**: Uses rule-based and pattern-matching techniques to identify leaked PII in model outputs.
- **Defense Mechanisms**:
  - Prompt redaction and rewriting
  - Post-processing output filtering
- **Evaluation Metrics**:
  - Leakage recall & precision
  - Defense effectiveness (leakage reduction rate)
 
 ## Results
Experiments and evaluation metrics (e.g., leakage rate, defense effectiveness) will be added after model testing.
> Stay tuned — detailed results and visualizations will be uploaded here.

## Research Plan
This project is under active development. The following directions are being considered:

- **[Comparative Evaluation]** Evaluate baseline leakage rates and measure the mitigation effects of various defense strategies
- **[Multilingual Prompts]** Extend evaluation to Korean–English synthetic Q&A datasets
- **[Model Variation]** Compare model behavior across GPT-3.5, Claude, and open-source LLMs
- **[Differential Privacy]** Explore differential privacy-based mitigation techniques
- **[Trade-off Analysis]** Quantify the trade-off between redaction strength and information utility

