# 🏛️ DAO Fund - Blockchain Technical Test

This project is a practical implementation of a **Decentralized Investment Fund (DAO Fund)** that consists of two main components:

1. **Smart Contract** — developed in **Solidity** on an EVM-compatible blockchain.
2. **Back-End** — developed with **FastAPI** and **Web3.py** to provide a REST API for interacting with the contract.

---

## 📁 Project Structure

```
dao-fund/
│
├── contracts/
│   └── DAOFund.sol              # DAO Fund Smart Contract
│
├── backend/
│   ├── main.py                   # FastAPI entry point
│   ├── routers/
│   │   ├── deposit.py            # API route for deposit and token minting
│   │   ├── proposals.py          # API route for creating/viewing proposals
│   │   ├── vote.py               # API route for voting
│   │   └── withdraw.py           # API route for withdrawal
│   ├── services/
│   │   └── blockchain_service.py # Handles blockchain interactions via Web3.py
│   ├── db/
│   │   ├── database.py           # Database setup (SQLite/PostgreSQL)
│   │   └── models.py             # ORM models for proposal, votes, users
│   ├── tests/
│   │   ├── test_contract.py      # Contract tests
│   │   └── test_api.py           # API tests
│   ├── requirements.txt
│   └── config.py                 # General configurations (RPC URL, contract address, etc.)
│
├── scripts/
│   └── deploy_contract.py        # Deployment script for test network
│
├── README.md
├── .gitignore
└── docker-compose.yml            # Optional - to run full stack easily
```

---

## ⚙️ Requirements

* Python 3.10+
* Node.js (for compiling Solidity contracts)
* Ganache or Hardhat for local test network
* MetaMask (optional for testing transactions)

---

## 🚀 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/blockapp.git
cd blockapp/backend
```

### 2. Create virtual environment and install dependencies

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the FastAPI app

```bash
uvicorn main:app --reload
```

API will be available at:
👉 [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 🔗 API Endpoints

| Method | Route      | Description                            |
| ------ | ---------- | -------------------------------------- |
| POST   | /deposit   | Deposit ETH and mint equivalent tokens |
| POST   | /proposals | Create a new proposal                  |
| POST   | /vote      | Cast a positive or negative vote       |
| GET    | /proposals | Retrieve proposals with vote results   |
| POST   | /withdraw  | Withdraw ETH based on token share      |

---

## 🧪 Tests

To verify system functionality, run:

```bash
pytest
```

---

## 🧱 Smart Contract Details

The **DAOFund** contract includes the following functionalities:

* Deposit ETH and receive **ERC20 tokens** representing DAO shares
* Create proposals for ETH transfers
* Token-based voting (1 token = 1 vote)
* Automatic proposal execution when more than 50% of total tokens vote in favor
* Token holders can **burn tokens** and withdraw their proportional ETH share

---

## 💡 Future Improvements

* Add **Time Lock** for proposal execution
* Full documentation with **Swagger** or **Postman**
* **JWT Authentication** for user management
* **Docker Compose** for quick deployment
* Add a web dashboard to visualize proposals and votes

---

## 📄 License

MIT License © 2025 **Ali Farhani**

---

## 📬 Contact

* **LinkedIn:** [https://www.linkedin.com/in/alifarhani/](https://www.linkedin.com/in/alifarhani/)
* **Medium:** [https://medium.com/@alifarhani7727315](https://medium.com/@alifarhani7727315)
* **Iran Blockchain Community:** [https://iranblockchain.org](https://iranblockchain.org)

---

آیا دوست داری من در مرحله بعد اسکلت پوشه‌ها و فایل‌های FastAPI (کد خالی قابل اجرا) را هم برایت بسازم تا مستقیم در پروژه قرار دهی؟
