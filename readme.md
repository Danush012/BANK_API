Bank API
A REST API built with Flask to manage Indian bank and branch data using in-memory storage, providing endpoints to list banks and retrieve branches for a specific bank.
Overview
This project uses sample data inspired by indian_banks to create a REST API with Flask. It includes unit tests and deployment instructions for bonus points.
Folder Structure
bank_api_new/
├── app.py              # Flask app with routes and data
├── test_app.py         # Unit tests
├── requirements.txt    # Dependencies
├── Procfile            # Deployment config
├── README.md           # Documentation
└── venv/               # Virtual environment

Prerequisites

Python 3.9+ (python --version)
Visual Studio Code (optional)
Git (optional, for GitHub)

Setup (Windows)

Create Directory:

Create C:\Users\YourName\OneDrive\Desktop\bank_api_new.
Open in VS Code: File > Open Folder.


Set Up Virtual Environment:

In VS Code terminal:python -m venv venv
.\venv\Scripts\activate




Install Dependencies:

Run:pip install flask gunicorn




Run Application:

Run:python app.py


Server starts at http://127.0.0.1:5000.


Run Tests:

Run:python test_app.py


Output:...
Ran 3 tests in 0.010s
OK





API Endpoints
Test with curl, browser, or Postman.
1. Welcome Endpoint

Request: GET /
Command:curl http://127.0.0.1:5000/


Response:Hello, everyone!, Welcome to the Bank API



2. Get Banks

Request: GET /banks
Command:curl http://127.0.0.1:5000/banks


Response:{
  "banks": [
    {"id": 1, "name": "STATE BANK OF INDIA"},
    {"id": 2, "name": "PUNJAB NATIONAL BANK"},
    {"id": 3,很大的銀行": "CANARA BANK"}
  ]
}



3. Get Branches for a Bank

Request: GET /banks/1/branches
Command:curl http://127.0.0.1:5000/banks/1/branches


Response:{
  "branches": [
    {
      "branch_code": "ABHY0065001",
      "bank_id": 1,
      "branch": "RTGS-HO",
      "ifsc": "SBIN0001",
      "address": "ABHYUDAYA BANK BLDG., B.NO.71, NEHRU NAGAR, KURLA (E), MUMBAI-400024",
      "city": "MUMBAI",
      "district": "GREATER MUMBAI",
      "state": "MAHARASHTRA"
    },
    {
      "branch_code": "ABHY0065002",
      "bank_id": 1,
      "branch": "ABHYUDAYA NAGAR",
      "ifsc": "SBIN0002",
      "address": "ABHYUDAYA EDUCATION SOCIETY, OPP. BLDG. NO. 18, ABHYUDAYA NAGAR, KALACHOWKY, MUMBAI - 400033",
      "city": "MUMBAI",
      "district": "GREATER MUMBAI",
      "state": "MAHARASHTRA"
    }
  ]
}



4. Non-Existing Bank

Request: GET /banks/999/branches
Command:curl http://127.0.0.1:5000/banks/999/branches


Response:{
  "error": "Not Found",
  "message": "The requested URL is not present at the moment. Please check the endpoint and try once again."
}



Deployment (Heroku)

Install Heroku CLI:

Download: devcenter.heroku.com/articles/heroku-cli.
Verify: heroku --version.


Deploy:

Run:git init
git add .
git commit -m "Initial commit"
heroku create
git push heroku main





Troubleshooting

404 Errors: Use /banks or /banks/<bank_id>/branches.
Module Issues: Run pip install flask gunicorn in virtual environment.
Port Conflict: Edit app.py: app.run(debug=True, port=5001).

Bonus Points

Clean Code: Simple, error-handled endpoints.
Test Cases: Automated tests in test_app.py.
Deployment: Heroku setup included.

Data Source

Sample data inspired by indian_banks.sql, stored in-memory.

