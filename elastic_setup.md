# Elastic Stack Setup Guide

This document describes how to recreate the Elasticsearch environment used in the Emergency Distress Intelligence System.

---

## 1️⃣ Create Index with Mapping

We created a structured index to store distress reports with geospatial capability.

```json
PUT distress-reports
{
  "mappings": {
    "properties": {
      "message": { "type": "text" },
      "urgency": { "type": "float" },
      "incident_type": { "type": "keyword" },
      "source": { "type": "keyword" },
      "contact": { "type": "keyword" },
      "location": { "type": "geo_point" }
    }
  }
}
