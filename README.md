# AI Incident Investigator

### An Intelligent, Explainable Financial Fraud Investigation System

**AI Incident Investigator** is an ongoing software engineering project that aims to transform suspicious financial transaction analysis into a structured, evidence-driven investigation workflow.

Rather than simply classifying a transaction as fraudulent or legitimate, the system is being designed to help investigators understand *why* a transaction may be suspicious, explore potentially connected accounts, trace transaction relationships, and generate structured investigation reports.

> **Project Status:** Early Development · Research & Engineering Project

---

## 1. Problem Statement

Financial fraud detection systems often focus on identifying suspicious transactions through classification or anomaly detection. However, identifying a potentially fraudulent transaction is only one part of an investigation.

Investigators may also need to understand:

- Why a transaction received a high-risk score.
- Which transaction characteristics contributed to its suspicious behaviour.
- Whether other accounts are potentially connected to the activity.
- How suspicious transactions relate to one another.
- What evidence supports an investigation.
- How findings can be presented in an understandable report.

This project aims to bridge the gap between transaction-level fraud detection and structured financial investigation.

## 2. Project Vision

The goal is to develop an AI-assisted investigation platform that follows a complete investigation workflow:

**Transaction → Risk Assessment → Relationship Analysis → Evidence Collection → Investigation Report**

The system will focus on combining machine learning, transaction analytics, relationship analysis, and AI-assisted explanations into one investigation-oriented application.

## 3. Core Features & Planned Capabilities

### 3.1 Transaction Investigation
- Browse and select individual financial transactions.
- Inspect transaction details and relevant attributes.
- Initiate an investigation for a selected transaction.

### 3.2 Fraud Risk Assessment
- Calculate a risk score for selected transactions.
- Identify potentially suspicious transaction patterns.
- Prioritize transactions for further investigation.
- Provide interpretable reasons behind risk assessments.

### 3.3 Connected Account Analysis
- Identify potentially related accounts through transaction relationships.
- Explore incoming and outgoing transaction connections.
- Investigate suspicious transaction patterns across connected accounts.
- Support relationship-based analysis and investigation.

### 3.4 AI-Assisted Investigation
- Convert analytical findings into understandable explanations.
- Summarize suspicious transaction behaviour.
- Connect model outputs and analytical evidence with investigation findings.
- Support investigators in understanding complex transaction activity.

### 3.5 Investigation Report Generation
- Generate structured reports for individual investigations.
- Include transaction details, risk assessment, and relevant findings.
- Present connected-account information and supporting evidence.
- Provide readable summaries for further review.

*Note: These are planned capabilities and will be implemented incrementally.*

## 4. Proposed Investigation Workflow

The intended user experience is:

1. **Select Transaction:** Choose a suspicious transaction from the available transaction records.
2. **Risk Score:** Analyze the transaction and calculate its risk level.
3. **Explore Connections:** Identify potentially related accounts and transaction relationships.
4. **Investigate Evidence:** Review relevant transaction details and analytical findings.
5. **Generate Report:** Produce a structured investigation report explaining the findings.

## 5. Dataset

The initial development uses the **PaySim Synthetic Financial Dataset**.

PaySim simulates mobile money transactions and provides transaction-level attributes useful for financial fraud analysis.

Initial dataset characteristics:

| Attribute | Value |
|---|---:|
| Total transactions | 6,362,620 |
| Fraudulent transactions | 8,213 |
| Fraud proportion | Approximately 0.1291% |
| Dataset type | Synthetic financial transactions |

The dataset contains a significant class imbalance, making fraud detection and evaluation particularly challenging.

**Dataset handling:** The original CSV is approximately 493.5 MB and is intentionally excluded from this GitHub repository. It will remain locally available during development.

## 6. Proposed Technical Direction

The architecture and technology stack will evolve as the project develops.

| Area | Proposed Direction |
|---|---|
| Programming Language | Python |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Backend | To be finalized |
| Investigation Logic | Transaction and relationship analysis |
| AI Integration | LLM-assisted explanations and summaries |
| Visualization | To be finalized |
| Testing | Pytest |
| Version Control | Git and GitHub |

Technology choices will be finalized based on implementation requirements and experimentation.

## 7. Proposed System Architecture

The system is intended to evolve into the following modular architecture:

```text
                 User Interface
                       |
                       v
             Investigation Workflow
                       |
          +------------+------------+
          |            |            |
          v            v            v
     Transaction   Risk Scoring   Account
      Analysis      Engine       Analysis
          |            |            |
          +------------+------------+
                       |
                       v
                Evidence Analysis
                       |
                       v
              AI-Assisted Reasoning
                       |
                       v
             Investigation Report
```

The architecture is conceptual and will be refined as individual components are implemented.

## 8. Repository Structure

```text
AI-Incident-Investigator/
│
├── Notebooks/
│   └── 01_eda.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── models/
├── reports/
├── src/
├── tests/
│
├── .gitignore
└── README.md
```

Large datasets, virtual environments, credentials, and other local-only files are excluded from version control.

## 9. Development Roadmap

| Phase | Focus | Status |
|---|---|---|
| Phase 1 | Project setup and dataset exploration | In Progress |
| Phase 2 | Data preprocessing and feature engineering | Planned |
| Phase 3 | Fraud detection and risk scoring | Planned |
| Phase 4 | Transaction relationship and account analysis | Planned |
| Phase 5 | Investigation evidence and reasoning | Planned |
| Phase 6 | AI-assisted investigation summaries | Planned |
| Phase 7 | Backend and user interface integration | Planned |
| Phase 8 | Investigation report generation | Planned |
| Phase 9 | Testing, evaluation, and documentation | Planned |

## 10. Research & Engineering Focus

Beyond building a functional application, the project aims to explore:

- Handling highly imbalanced financial transaction datasets.
- Interpretable fraud risk assessment.
- Relationship-based financial transaction analysis.
- Evidence-driven investigation workflows.
- Explainable AI for financial investigations.
- Reliability and evaluation of AI-generated investigation summaries.

An important design principle is that AI-generated explanations should be grounded in available transaction evidence rather than presented as unsupported conclusions.

## 11. Getting Started

### Clone the repository

```bash
git clone https://github.com/Umaima-Mughal/Ai-Incident-Investigator.git
cd Ai-Incident-Investigator
```

### Create a virtual environment

```bash
python -m venv .venv
```

### Activate on Windows

```powershell
.venv\Scripts\Activate.ps1
```

### Install dependencies

Dependency installation instructions will be added once the project's dependency file is established.

### Prepare the dataset

Place the PaySim CSV file inside:

```text
data/raw/
```

### Open the exploratory notebook

Open `Notebooks/01_eda.ipynb` using Jupyter Notebook or VS Code.

## 12. Current Implementation

The project is in its early development stage.

Currently:
- Project repository initialized.
- PaySim dataset selected.
- Initial exploratory data analysis notebook added.
- Project scope and investigation workflow defined.

Implementation details and completed capabilities will be updated as development progresses.

## 13. Disclaimer

This project is intended for educational, research, and software engineering purposes.

The system is designed to assist with the analysis of potentially suspicious financial activity. A high-risk score or an AI-generated explanation does not establish that fraud has occurred. All findings require appropriate verification and human review.

---

**Developed as an ongoing Software Engineering project.**
