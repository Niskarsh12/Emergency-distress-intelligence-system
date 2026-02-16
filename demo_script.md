# 🎥 Demo Script – Emergency Distress Intelligence System (EDIS)

## 1️⃣ Introduction (0:00 – 0:20)

Hello, I’m Nishkarsh.

This is EDIS — Emergency Distress Intelligence System.

EDIS converts unstructured distress messages into real-time geospatial urgency heatmaps to help emergency teams prioritize critical cases faster.

---

## 2️⃣ The Problem (0:20 – 0:40)

During disasters, authorities receive hundreds or thousands of text-based distress reports.

These messages are:
- Unstructured
- Hard to prioritize
- Time-sensitive

Manual review delays life-saving response.

---

## 3️⃣ The Solution (0:40 – 1:10)

EDIS ingests distress messages into Elasticsearch.

Each message includes:
- Geo location (`geo_point`)
- Incident metadata
- Urgency score (0 to 1)

Using Elastic Maps:
- We generate a heatmap based on aggregated urgency
- High-risk zones appear red
- Lower-risk zones appear blue/green

This instantly shows where help is needed most.

---

## 4️⃣ Live Demo (1:10 – 1:40)

Here you can see:

- The urgency heatmap layer (sum of urgency)
- Individual distress case points

Clicking a case shows:
- Exact message
- Location
- Urgency score
- Contact information

Critical cases (e.g., medical emergencies) are clearly visible and prioritized.

---

## 5️⃣ Human-in-the-Loop (1:40 – 1:55)

When urgency exceeds a threshold, cases are escalated to human emergency coordinators.

AI assists — humans decide.

---

## 6️⃣ Conclusion (1:55 – 2:00)

EDIS transforms chaos into actionable intelligence.

From unstructured distress signals to real-time emergency prioritization — powered entirely by the Elastic Stack.
