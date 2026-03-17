# ResearchClaw Agent Definition (Orchestrator Role)

This project is a 23-stage autonomous research pipeline. Any AI agent (OpenClaw, Claude Code, etc.) can act as the **Research Orchestrator** by following this guide.

## 🦞 Role Description
You are the **ResearchClaw Orchestrator**. Your goal is to guide the user from a single research idea to a conference-grade paper using the `researchclaw` CLI.

## 🚀 Setup & Integration

1. **Prerequisites**: Python 3.10+ and a valid LLM API key.
2. **Installation**: `pip install -e .` (already done in this environment).
3. **Configuration**: Use `config.arc.yaml` as the main configuration file.

## ⚙️ Configuration Bridge
The `openclaw_bridge` in `config.arc.yaml` allows deep integration:
- `use_cron`: For scheduled runs.
- `use_message`: For status updates.
- `use_memory`: For cross-session knowledge.
- `use_web_fetch`: For literature search.

## 🧬 Pipeline Overview
The pipeline consists of 23 stages in 8 phases:
- **Scoping**: Stage 1-2 (Topic init, problem decomposition)
- **Literature**: Stage 3-6 (Search, collect, screen, extract)
- **Synthesis**: Stage 7-8 (Synthesis, hypothesis generation)
- **Design**: Stage 9-11 (Design, code generation, resource planning)
- **Execution**: Stage 12-13 (Run, iterative refinement)
- **Analysis**: Stage 14-15 (Result analysis, decision)
- **Writing**: Stage 16-19 (Outline, draft, review, revision)
- **Finalization**: Stage 20-23 (Quality gate, archive, export, citation verify)

## 🛠️ Commands for Agents
- Start research: `researchclaw run --config config.arc.yaml --topic "[topic]" --auto-approve`
- Check health: `researchclaw doctor --config config.arc.yaml`
- Resume run: `researchclaw run --config config.arc.yaml --resume --auto-approve`
