# Emergency Distress Intelligence System (EDIS)

A real-time emergency intelligence system that converts unstructured human distress messages into **geospatial urgency heatmaps**, enabling faster prioritization and human-coordinated disaster response.

---

## 🚨 Problem

During disasters (floods, earthquakes, medical emergencies), help requests arrive as **unstructured text**:
- WhatsApp messages
- Social media posts
- Helpline transcripts
- SMS alerts

These messages:
- Lack structure
- Are hard to prioritize
- Do not provide a real-time spatial overview
- Overwhelm human responders

As a result, **critical cases (infants, medical emergencies)** can be delayed while less urgent cases consume attention.

---

## 💡 Solution

EDIS transforms raw distress messages into an **actionable geospatial intelligence layer** using Elastic.

It:
1. Ingests unstructured emergency messages
2. Extracts location, urgency, and incident context
3. Scores distress severity
4. Visualizes cumulative urgency as a **heatmap**
5. Enables **human-in-the-loop escalation** for decision-making

---

## 🧠 Key Capabilities

### 🔹 Semantic Urgency Scoring
Each incoming message is analyzed to derive an **urgency score** based on:
- Medical keywords (infant, diabetic, bleeding, etc.)
- Situation severity
- Contextual risk indicators

This avoids naïve “count-based” prioritization.

---

### 🔹 Geospatial Indexing
Messages are indexed with:
- `geo_point` location
- urgency score
- incident metadata

This allows real-time spatial aggregation.

---

### 🔹 Distress Heatmap Visualization
Using **Elastic Maps**, the system generates:
- A **heatmap layer** showing cumulative distress intensity
- Brighter zones = higher urgency concentration
- Responders instantly see where attention is needed most

---

### 🔹 Individual Case Drill-Down
Alongside the heatmap:
- Individual emergency reports remain clickable
- Responders can inspect message content and context
- Enables verification and escalation

---

### 🔹 Human-in-the-Loop Escalation
EDIS does **not replace humans**.

Instead, it:
- Flags high-urgency zones
- Surfaces critical cases
- Allows human coordinators to take final action:
  - Contact NGOs
  - Dispatch rescue teams
  - Coordinate medical aid

---

## 🗺️ System Architecture

Distress Message

↓

Semantic Analysis & Urgency Scoring

↓

Elasticsearch (Geo + Metadata Indexing)

↓

Elastic Maps

├─ Distress Heatmap (Aggregated Urgency)

└─ Individual Emergency Case Points

↓

Human Emergency Coordinators

↓

Rescue & Aid Response


---

## 📊 Visualization Layers

### 1️⃣ Distress Intensity Heatmap
- Aggregation: `sum(urgency)`
- Purpose: Identify **priority zones**, not just dense areas

### 2️⃣ Individual Emergency Reports
- Clickable points
- Shows message details
- Enables on-ground coordination

---

## 🧪 Demo Scenario

**Flood-affected city area**

Sample message:
> “No insulin left, diabetic patient, water rising fast.”

Result:
- High urgency score
- Contributes strongly to local heatmap
- Visible immediately to coordinators
- Prioritized over lower-risk cases

---

## 🛠️ Tech Stack

- **Elasticsearch** – indexing, aggregation, geo queries
- **Elastic Maps** – heatmaps & geospatial visualization
- **Elastic ML / AI tooling** – semantic understanding (conceptual)
- **KQL / Filters** – interactive exploration

---

## 🚀 Why This Matters

- Moves from *reactive* to *proactive* disaster response
- Scales naturally as message volume increases
- Works with real-world messy data
- Keeps humans in control
- Built entirely on Elastic’s ecosystem

---

## 🏆 Hackathon Value

This project demonstrates:
- Practical use of Elastic Maps
- Meaningful geospatial aggregation
- Real-world emergency application
- Clear human-AI collaboration
- Production-relevant architecture

---

## 📌 Future Extensions

- NGO capacity overlays
- Live responder tracking
- Temporal heatmaps (how urgency evolves)
- Automated NGO notification workflows
- Multi-language distress parsing

---

## 👤 Author

Built solo as part of an online hackathon.

