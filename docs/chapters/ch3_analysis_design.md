
## 3.3 Use Case Analysis
- Actors: Patient, Medical Administrator, AI & OCR Engine.
- UC-01 Ingest Lab Report: User submits report (PDF/Image); engine extracts metrics.
- UC-02 Verify Extraction: User confirms or edits parsed values before persistence.
- UC-03 Longitudinal Tracking: Historical metrics are plotted against clinical thresholds.
- UC-04 AI Health Triage: User queries results; LLM generates lay explanations with strict non-diagnostic disclaimers.
- UC-05 Automated Screening Alerts: Rule engine schedules preventive checkups.

## 3.4 Sequence Flow & Safety Pattern
The ingestion sequence implements human-in-the-loop validation:
1. Client transmits file to `/api/reports/upload`.
2. Engine extracts raw metrics and runs deterministic range checks.
3. System holds state in draft mode until user confirms accuracy.
4. Confirmed metrics persist to MongoDB `biometric_records`.
