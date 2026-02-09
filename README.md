ERP Financial Monitoring & ML Anomaly Detection Pipeline 

Project Overview
Automated Microsoft Fabric pipeline that ingests ERP CSV files via OneLake file triggers, processes financial data across records through Bronze→Silver→Gold medallion layers, and delivers real-time ML anomaly detection with CFO email summaries.

Live Results: 27 HIGH priority budget alerts, €5.1M reallocation recommendations, +8% growth forecasts.

🏗️ Architecture
ERP CSV Drop → OneLake Trigger → Bronze (Raw) → Silver (Clean) → Gold (ML)
                                                    ↓
                                    Python/Spark Summary → SMTP CFO Email

                                    
                                    
                                    <img width="1308" height="299" alt="Screenshot 2026-02-09 at 2 43 40 PM" src="https://github.com/user-attachments/assets/89c50d71-4f6d-4fe5-99b9-6975d12aee25" />
<img width="1070" height="622" alt="Screenshot 2026-02-09 at 2 45 25 PM" src="https://github.com/user-attachments/assets/f290c655-54e7-4760-8d8d-04c1d4f3528c" />

<img width="1364" height="758" alt="Screenshot 2026-02-09 at 2 49 58 PM" src="https://github.com/user-attachments/assets/7e337cc2-50db-44a9-ba77-3c4d7d8e409e" />

<img width="4" height="10" alt="Screenshot 2026-02-09 at 2 53 56 PM" src="https://github.com/user-attachments/assets/9e328d5a-6478-436c-843d-2d4860e9f0f1" />

<img width="1423" height="721" alt="Screenshot 2026-02-09 at 2 54 04 PM" src="https://github.com/user-attachments/assets/c6693194-7138-4e0a-96ba-7154fbdbd87f" />

<img width="1456" height="746" alt="Screenshot 2026-02-09 at 2 54 17 PM" src="https://github.com/user-attachments/assets/5e7a1cf9-c17b-4b20-b38b-182c409313ee" />

                                    

🔧 Tech Stack
Microsoft Fabric (Lakehouse, Pipelines, Notebooks)
PySpark / Python 3.10+
ML: Isolation Forest, Z-Score anomaly detection
SMTP: Gmail API integration
Storm Technology Solver CPM integration

🚀 How It Works
text
1. ERP CSV → Files/erp_input/*.csv (OneLake)
2. ERP_AutoTrigger → Solver_pipeline executes
3. Bronze→Silver→Gold → ML anomaly scoring  
4. sending_mail notebook → 5-line summary email
5. CFO inbox: "27 HIGH alerts, €5.1M reallocate, +8% forecast"

