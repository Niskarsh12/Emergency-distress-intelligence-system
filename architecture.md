
---

# 📄 architecture.md

```markdown
# System Architecture

## Overview

The Emergency Distress Intelligence System transforms unstructured distress messages into actionable geospatial intelligence using Elasticsearch and Elastic Maps.

---

## Flow of Data

Distress Message (Unstructured Text)
        ↓
Semantic Analysis & Urgency Scoring
        ↓
Elasticsearch Indexing
        ↓
Geo Point Mapping
        ↓
Heatmap Aggregation (sum of urgency)
        ↓
Dashboard Visualization
        ↓
Human Emergency Escalation

---

## Components

### 1️⃣ Data Layer
- Elasticsearch index: `distress-reports`
- Fields:
  - message (text)
  - urgency (float)
  - incident_type (keyword)
  - location (geo_point)
  - contact (keyword)

---

### 2️⃣ Intelligence Layer
- Urgency scoring (0–1 scale)
- ES|QL for sorting and prioritization
- Aggregation-based heat intensity mapping

---

### 3️⃣ Visualization Layer
- Elastic Maps heatmap (distress density)
- Individual case point markers
- Interactive inspection tooltips
- Dashboard integration

---

### 4️⃣ Human-in-the-Loop Escalation

High urgency cases are:
- Identified via urgency score
- Surfaced visually in heatmap clusters
- Routed to human coordinators for verification and response

---

## Design Principles

- Real-time geospatial awareness
- Data-driven prioritization
- Minimal infrastructure complexity
- Built fully on Elastic Stack
- Human escalation for safety validation

---

This architecture enables rapid crisis triage using semantic analysis and spatial aggregation.
