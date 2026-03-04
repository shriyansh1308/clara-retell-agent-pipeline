# Clara Answers – Retell Agent Automation Pipeline

## Overview

This project builds a zero-cost automation pipeline that converts demo call transcripts into structured Retell voice agent configurations.

The system simulates how Clara Answers converts real-world customer conversations into deployable AI voice agents.

## Pipeline Architecture

Demo Call Transcript  
↓  
Extract structured information  
↓  
Generate Account Memo JSON (v1)  
↓  
Generate Retell Agent Draft Spec (v1)  

Onboarding Call  
↓  
Update Account Memo  
↓  
Generate Agent Spec (v2)  
↓  
Create Change Log  

## Project Structure
outputs/
└ accounts/
└ account_1/
├ v1/
│ ├ account_memo.json
│ └ agent_spec.json
└ v2/
├ account_memo.json
├ agent_spec.json
└ changes.json


## Outputs

Each account generates:

- **Account Memo JSON** – structured operational data
- **Agent Spec JSON** – configuration for Retell voice agent
- **Versioned updates** (v1 → v2)
- **Change log** documenting onboarding updates

## Technologies Used

- Python
- JSON for structured storage
- Google Colab for pipeline execution
- GitHub for repository management

## How to Run

1. Upload demo transcripts into `inputs/demo_calls`
2. Run the pipeline notebook
3. Generated outputs appear in `outputs/accounts/`

## Limitations

- Uses simple rule-based extraction instead of a full NLP pipeline.
- Demo transcript data may contain incomplete fields.

## Future Improvements

- Automatic speech-to-text transcription
- Full automation using workflow tools like n8n
- Improved information extraction using NLP models
