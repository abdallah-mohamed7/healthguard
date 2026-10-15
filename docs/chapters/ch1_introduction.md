# Chapter 1: Introduction

## 1.1 Context and Motivation
Chronic non-communicable diseases (NCDs)—including cardiovascular conditions, type 2 diabetes mellitus, and hypertension—represent the predominant cause of global mortality and long-term morbidity (World Health Organization, 2022). A critical bottleneck in reducing NCD burdens is late-stage detection. Routine biometric tracking and laboratory screenings are proven to intercept pathological trajectories early; however, adherence to regular screening intervals remains suboptimal among the general public.

Patients frequently face three key barriers:
1. Fragmented record-keeping across disparate healthcare facilities.
2. Low health data literacy, rendering complex laboratory panels unintelligible to lay individuals.
3. Lack of proactive tracking, resulting in missed appointments and overlooked long-term biometric trends.

## 1.2 Problem Statement
Existing patient-facing healthcare applications suffer from acute trade-offs: they either act as passive, disconnected cloud storage vaults for raw PDF documents without computational understanding, or they present opaque, non-deterministic predictive models lacking safety guardrails. When patients receive laboratory reports containing parameters such as HbA1c, lipid profiles, and fasting blood glucose, the absence of contextual longitudinal tracking prevents early awareness of gradual deteriorations. Consequently, critical preventive interventions are missed until clinical symptoms manifest.

## 1.3 Proposed Solution: HealthGuard
HealthGuard is a preventive healthcare platform (Web and Mobile) engineered to bridge the operational gap between diagnostic laboratories and patient self-management. The platform implements an end-to-end analytical pipeline:
- Ingestion & OCR: Users capture or upload multi-format laboratory reports. An automated OCR extraction engine extracts analytical metrics, units, and reference intervals.
- Longitudinal Biometric Tracking: Extracted metrics are persisted into structured time-series health records, visualizing temporal shifts against medically validated baseline thresholds.
- Safe AI Triage: An LLM-driven explanation engine interprets complex laboratory nomenclature into plain language, bound by strict deterministic clinical guardrails and explicit non-diagnostic disclaimers (Topol, 2019).
- Automated Screening Scheduler: A rule-based reminder engine schedules upcoming laboratory tests based on age, gender, and observed physiological trends.

## 1.4 Project Objectives
1. Implement a cross-platform data collection interface (React/TypeScript and Android).
2. Automate tabular metric parsing from laboratory documents with structured schema validation.
3. Establish a deterministic clinical safety layer that overrides generative model outputs to ensure patient safety.
4. Provide verifiable automated end-to-end testing across data ingestion, persistence, and reminder pipelines.

## References
1. World Health Organization. (2022). *Noncommunicable diseases country profiles 2022*. World Health Organization.
2. Topol, E. J. (2019). High-performance medicine: the convergence of human and artificial intelligence. *Nature Medicine*, 25(1), 44-56.
