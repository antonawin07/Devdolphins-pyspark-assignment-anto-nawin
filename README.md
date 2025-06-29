# PySpark Data Engineer Take-Home Assignment – Anto Nawin

## 📌 Problem Overview
This project simulates a real-time data processing pipeline using PySpark on Databricks. It reads transaction data in chunks, detects specific patterns, and outputs matched results to AWS S3 while using PostgreSQL for temporary state tracking.

## 🧰 Tech Stack
- PySpark (Databricks)
- AWS S3
- PostgreSQL
- Python (pandas, boto3)
- GitHub, Loom

## 🛠️ Components
### 🔹 Mechanism X
- Reads 10,000 rows per second from `transactions.csv`
- Uploads each chunk to AWS S3 (`input/` folder)

### 🔹 Mechanism Y
- Listens for new chunks on S3
- Ingests and applies 3 detection patterns using PySpark:
    - **PatId1**: UPGRADE high-activity, low-weight customers
    - **PatId2**: CHILD low-value, high-frequency users
    - **PatId3**: DEI-NEEDED for gender imbalance

- Stores detection results to S3 (`output/`), 50 per file
- Uses PostgreSQL for merchant transaction tracking

## 🧾 File Structure
```
.
├── databricks_notebooks/
│   └── pattern_detection_y.ipynb
├── scripts/
│   ├── mechanism_x_chunk_uploader.py
│   └── postgres_setup.sql
├── output_sample/
│   └── detections_sample.csv
├── docs/
│   ├── architecture.png
│   └── assumptions.md
├── requirements.txt
└── README.md
```

## 📥 Loom Videos
- **Live Demo**: [your-demo-link]
- **Code Walkthrough**: [your-code-link]
- **Setup Explanation**: [your-setup-link]
- **Sample Output**: [your-output-link]
- **Architecture Explanation**: [your-architecture-link]

## 📦 Sample Output
See `output_sample/detections_sample.csv` for an example of formatted detection results.

## 📝 Assumptions
Listed in `docs/assumptions.md`.

## 📌 Notes
This project was completed as a real-time simulation to showcase readiness for high-performance PySpark Data Engineering roles.
