# Architecture & Tech Stack Decisions

## ADR-001: Core Platform Stack
- Status: Accepted
- Frontend: React + TypeScript
- Mobile: Android Native
- Backend: Flask REST API
- Primary Database: MongoDB
- AI Engines: Gemini (multimodal) + Groq (low-latency inference)
- Grounding: Local/Vector RAG for clinical preventive triage
- Testing Strategy: Pytest (Backend) + Playwright (E2E)
- Infrastructure: Docker + GitHub Actions CI/CD
