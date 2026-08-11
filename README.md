# securitisation-risk-observatory
# Securitisation Risk Observatory

A data analytics platform for **securitisation risk assessment, loan pool surveillance, IFRS 9 ECL analysis, and stress testing**.

## 📌 Project Overview

The **Securitisation Risk Observatory** is a risk analytics platform designed to analyze securitised loan pools using assumed bank SAP/ERP data.

The platform provides a dashboard for monitoring:

* Loan pool performance
* Delinquency and DPD distribution
* IFRS 9 credit risk stages
* Expected Credit Loss (ECL)
* Credit enhancement
* Credit spread
* Loan-level analytics
* CSV data ingestion
* Stress testing

The project is designed as a practical implementation of a **Data Analyst / Risk Analytics** solution for securitisation.

---

## 🎯 Project Objectives

The main objectives of this project are:

1. Analyze securitised loan pools.
2. Monitor loan delinquency and credit risk.
3. Analyze IFRS 9 credit risk stages.
4. Calculate and monitor Expected Credit Loss (ECL).
5. Perform stress testing under different scenarios.
6. Provide useful analytics for investors and risk teams.
7. Build an interactive securitisation risk dashboard.
8. Create a foundation for advanced waterfall and risk simulation analysis.

---

## 🖥️ Dashboard Features

### 1. Loan Pool Surveillance

The dashboard provides key portfolio indicators including:

* Pool Balance
* Number of Loans
* Weighted Average DPD
* 30+ DPD
* IFRS 9 ECL
* Credit Spread
* Credit Enhancement

### 2. IFRS 9 Credit Risk Analysis

The dashboard displays credit risk stage distribution:

* Stage 1
* Stage 2
* Stage 3

This helps monitor the distribution of expected credit losses across different credit-risk stages.

### 3. DPD Distribution

The platform monitors delinquency buckets:

* Current
* 1–29 DPD
* 30–59 DPD
* 60–89 DPD
* 90+ DPD
* Default

### 4. Loan Pool Analytics

The platform provides basic loan pool metrics such as:

* Total Loans
* Total Balance
* Average Loan Balance
* 30+ DPD
* Weighted Average DPD
* Credit Enhancement

### 5. CSV Data Upload

Users can upload loan-level CSV files through the dashboard.

The backend validates the uploaded file and provides:

* Filename
* Number of rows
* Number of columns
* Validation status

---

## 🏗️ Project Architecture

```text
Securitisation Risk Observatory
│
├── backend
│   ├── server.py
│   ├── requirements.txt
│   └── .env
│
├── frontend
│   ├── public
│   ├── src
│   ├── package.json
│   ├── craco.config.js
│   ├── tailwind.config.js
│   └── ...
│
└── README.md
```

### Application Flow

```text
CSV / Bank Data
       │
       ▼
   FastAPI Backend
       │
       ▼
 Data Validation
       │
       ▼
 Analytics API
       │
       ▼
 React Dashboard
       │
       ▼
 Risk Monitoring
```

---

## 🛠️ Technologies Used

### Frontend

* React.js
* Axios
* Recharts
* Lucide React
* CRACO
* Tailwind CSS

### Backend

* Python
* FastAPI
* Uvicorn
* Pandas
* NumPy
* Pydantic

### Database / Infrastructure

* MongoDB
* Motor
* PyMongo

### Development Tools

* Git
* GitHub
* Visual Studio Code

---

## 📊 Project Datasets

The project uses assumed SAP/ERP-style securitisation data.

The main datasets include:

```text
auto_loan_securitisation_data.csv
dpd_snapshot_history.csv
static_pool_vintage_data.csv
dynamic_loss_monthly.csv
```

These datasets support loan-level analysis, delinquency analysis, vintage analysis, and monthly loss analysis.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/securitisation-risk-observatory.git
```

Move into the project:

```bash
cd securitisation-risk-observatory
```

---

# 🚀 Backend Setup

Go to the backend directory:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
python -m uvicorn server:app --reload --port 8001
```

Backend will run at:

```text
http://localhost:8001
```

API documentation is available at:

```text
http://localhost:8001/docs
```

---

# 🎨 Frontend Setup

Open another terminal.

Go to:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the React application:

```bash
npm start
```

Frontend will run at:

```text
http://localhost:3000
```

---

## 🔌 API Endpoints

### Health / Root

```http
GET /api/
```

### Dashboard Overview

```http
GET /api/overview
```

Returns:

* Pool information
* KPIs
* IFRS 9 stages
* DPD data
* Vintage data
* Monthly loss data
* Dataset information

### CSV Upload

```http
POST /api/upload
```

Used to upload and validate CSV files.

### Stress Testing

```http
POST /api/stress
```

Supports scenario parameters for:

* Default shift
* Recovery shift
* Prepayment shift

---

## 📈 Future Development

The current platform is the foundation for a more advanced securitisation analytics system.

Planned features include:

### IFRS 9 ECL Engine

```text
PD × LGD × EAD
```

with:

* Stage 1 analysis
* Stage 2 analysis
* Stage 3 analysis
* Expected credit loss monitoring

### Stress Testing Framework

Scenario analysis for:

* Increased defaults
* Reduced recoveries
* Changes in prepayment
* Increased delinquency

### Waterfall Analysis

Model cash-flow distribution across securitisation structures, including:

* Senior notes
* Mezzanine notes
* Junior/subordinated notes
* Interest payments
* Principal payments
* Credit enhancement

### Investor Reporting

Create reporting views for:

* Portfolio performance
* Loss trends
* Delinquency
* ECL
* Credit enhancement
* Stress scenarios

### Securitisation Risk Arena

A gamified simulation environment where users can analyze securitisation scenarios and historical crisis situations through a data analytics perspective.

---

## 🔐 Data Disclaimer

This project uses **assumed/demo SAP/ERP-style data** for educational and project-development purposes.

It does not represent actual confidential bank, customer, or investor information.

---

## 👨‍💻 Project Purpose

This project was developed as a **Data Analytics / Risk Analytics project** to demonstrate practical skills in:

* Python
* Pandas
* FastAPI
* React
* Data visualization
* Financial risk analytics
* Loan portfolio analysis
* IFRS 9 concepts
* Stress testing
* API development

---

## 📌 Current Status

**Version:** 1.0

### Completed

* [x] FastAPI backend
* [x] React frontend
* [x] Dashboard
* [x] Loan pool KPIs
* [x] IFRS 9 stage visualization
* [x] DPD distribution
* [x] Dataset overview
* [x] Loan pool analytics
* [x] CSV upload and validation
* [x] Stress testing API foundation

### Planned

* [ ] Real dataset-driven calculations
* [ ] Advanced IFRS 9 ECL engine
* [ ] Advanced stress testing
* [ ] Securitisation waterfall
* [ ] Investor reporting
* [ ] Risk Arena simulation
* [ ] Historical securitisation crisis analysis

---

## ⭐ Author

**Vishal Sonwane**

Computer Engineering | Data Analytics | Risk Analytics
