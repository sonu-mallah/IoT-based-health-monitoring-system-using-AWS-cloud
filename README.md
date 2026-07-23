# IoT-Based Health Monitoring System using AWS Cloud

A cloud-based Remote Patient Monitoring (RPM) system that simulates real-time patient vital signs, securely transmits health data using MQTT, processes data through AWS serverless services, stores patient records in Amazon DynamoDB, performs Machine Learning-assisted risk prediction, and visualizes patient health using an interactive Streamlit dashboard.

---

## Key Features

- Real-time patient vital monitoring
- MQTT-based IoT communication
- AWS IoT Core integration
- AWS Lambda for serverless data processing
- Amazon DynamoDB for cloud data storage
- Rule-based emergency detection
- Random Forest-based Machine Learning-assisted risk prediction
- Interactive Streamlit dashboard
- Historical patient vital trends
- Doctor notes management
- PDF report generation
- Automatic dashboard refresh

---

# System Architecture

```text
Patient Simulator
        │
        ▼
MQTT Protocol
        │
        ▼
AWS IoT Core
        │
        ▼
AWS Lambda
  ├── Payload Validation
  ├── Rule-Based Risk Detection
  └── Data Processing
        │
        ▼
Amazon DynamoDB
  ├── patient_info
  ├── rpm_data
  └── doctor_notes
        │
        ▼
Streamlit Dashboard
  ├── Real-Time Monitoring
  ├── Machine Learning Risk Prediction
  ├── Historical Trend Analysis
  ├── Doctor Notes
  └── PDF Report Generation
```

---

# Database Design

## Database Design

| patient_info (Static Data) | rpm_data (Dynamic Vitals) | doctor_notes |
|----------------------------|---------------------------|--------------|
| patient_id (PK) | patient_id (PK) | patient_id (PK) |
| name | timestamp (SK) | note_id (SK) |
| age | heart_rate | doctor_name |
| gender | respiratory_rate | note_text |
| height | temperature | timestamp |
| weight | spo2 | |
| | systolic_bp | |
| | diastolic_bp | |
| | risk_flag | |

# design decision
The database schema separates static patient information, real-time vital signs, and doctor observations into independent DynamoDB tables, improving data organization, scalability, and query efficiency.


#
# Technology Stack

## Programming

- Python

---

## Cloud Services

- AWS IoT Core
- AWS Lambda
- Amazon DynamoDB
- Boto3

---

## Machine Learning

- Scikit-learn
- Random Forest Classifier
- Joblib

---

## Dashboard

- Streamlit
- Pandas
- Plotly

---

## Communication

- MQTT Protocol
- Eclipse Paho MQTT Client

---

# Project Workflow

1. Simulated patient vital signs are generated.
2. Patient data is published to AWS IoT Core through MQTT.
3. AWS Lambda validates incoming payloads and performs rule-based health checks.
4. Processed patient data is stored in Amazon DynamoDB.
5. The Streamlit dashboard retrieves patient information.
6. A Random Forest model performs Machine Learning-assisted risk prediction.
7. Doctors monitor patient status, review trends, add notes, and generate PDF reports.

---

# Dashboard Modules

### Overview

- Total Patients
- Critical Patients
- Warning Patients
- Live Patient Status

### Patient Monitor

- Patient Search
- Live Vital Signs
- Risk Prediction
- Historical Trends
- Doctor Notes
- PDF Report

---

# Skills Demonstrated

- IoT Communication
- MQTT Messaging
- Cloud Computing
- AWS Serverless Architecture
- Amazon DynamoDB
- Python Development
- Machine Learning Integration
- Data Visualization
- Database Design
- Real-Time Monitoring
- Exception Handling
- Debugging & Troubleshooting

---

# Future Improvements

- Multi-device support
- SMS / Email alerts
- Role-based authentication
- Docker deployment
- Kubernetes deployment
- Real IoT sensor integration
- Mobile application
- Analytics dashboard

---

# Author

**Sonu Mallah**
