This is a simple web application that simulates the lifecycle of a Health Savings Account or HSA for short. 

---

## Tech Stack Used:
- **Backend:** Python + Flask  
- **Frontend:** Flask templates (HTML) + CSS  
- **Storage:** JSON file (`database.json`) for local persistence  

## Setup & Run Locally

> Requires **Python 3.10+**

```bash
# 1. Clone repo
git clone https://github.com/<your-username>/HSA_Demo.git
cd HSA_Demo

# 2. (optional) create virtual environment
python3 -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Initialize empty database
echo "[]" > database.json

# 5. Run the app
python app.py 

```
Open your browser at 👉 http://localhost:5000

## How to Use
- Create Account with name + email (email must be unique).
- Open Account again later using your email.
- Deposit Funds into your HSA.
- Issue Card to get a virtual debit card number.
- Validate Transaction by entering amount + expense type:
  - Allowed: doctor, prescription, dental, vision, therapy, lab
  - Denied if not in list or insufficient balance.
- View Transaction History (date, type, amount, status).

## Project Architecture
Frontend (HTML + CSS templates)  
↓  
Flask Routes (app.py)  
↓  
Business Logic Functions  
↓  
JSON Storage (database.json)


