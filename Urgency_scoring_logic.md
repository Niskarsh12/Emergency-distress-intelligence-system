# Urgency Scoring Logic

## Overview

The Emergency Distress Intelligence System (EDIS) converts unstructured human distress messages into structured, geospatial intelligence. 

A core component of this process is the **Urgency Scoring Model**, which assigns a numerical score (0.0 – 1.0) to each emergency report to enable prioritization and heatmap aggregation.

This scoring allows:
- Faster identification of critical incidents
- Heatmap intensity visualization
- Human-in-the-loop escalation
- Resource prioritization

---

## Why Urgency Scoring?

Raw distress messages vary significantly in severity:

- "No food for baby"
- "Minor injury"
- "No insulin left, diabetic patient"
- "Flood water rising rapidly"

Without structured scoring, all reports appear equal.

Urgency scoring transforms qualitative distress into **quantitative intelligence**.

---

## Scoring Range

Each report is assigned a value between:

- **0.0 → Low urgency**
- **1.0 → Extreme / life-threatening urgency**

Example:

| Scenario | Urgency Score |
|----------|---------------|
| Minor assistance needed | 0.30 |
| Medical supply shortage | 0.70 |
| Infant without food | 0.85 |
| Critical medical dependency (e.g., insulin) | 0.95 |

---

## Factors Influencing Urgency

Urgency scoring considers multiple dimensions:

### 1. Medical Severity
- Mentions of critical conditions (e.g., insulin dependency, bleeding)
- Presence of vulnerable individuals (infants, elderly)

### 2. Resource Deprivation
- No food
- No clean water
- No medication

### 3. Environmental Risk
- Flood water rising
- Fire
- Structural collapse
- Trapped individuals

### 4. Vulnerable Groups
- Baby / infant
- Pregnant woman
- Elderly
- Disabled individuals

---

## Aggregation for Heatmap

In Elastic Maps, urgency values are aggregated using:


This creates a **distress intensity heatmap**, where:

- Higher concentration of high-urgency reports → hotter regions
- Lower urgency reports → cooler regions

This enables:

- Visual prioritization
- Geospatial clustering of crisis zones
- Rapid situational awareness

---

## Human-in-the-Loop Escalation

If urgency exceeds a defined threshold (e.g., 0.85):

- Case is escalated to human emergency coordinators
- Immediate response workflow is triggered
- Resource matching and dispatch coordination begins

This prevents:
- AI-only decision making
- False prioritization
- Over-automation in critical scenarios

---

## Design Philosophy

The urgency scoring system follows three principles:

1. **Transparency** – Scores are explainable and interpretable.
2. **Prioritization** – Critical lives first.
3. **Augmentation, not replacement** – AI supports human responders.

---

## Future Improvements

- NLP-based dynamic scoring
- Historical incident weighting
- Real-time environmental data integration
- Adaptive threshold learning

---

## Conclusion

Urgency scoring is the bridge between raw human distress signals and actionable emergency intelligence.

It enables EDIS to move from message processing to life-saving prioritization.


