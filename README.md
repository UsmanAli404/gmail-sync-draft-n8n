# Gmail Sync + Transform + Store Draft (n8n Workflow)

This workflow connects to Gmail, pulls new messages, converts them into structured API-ready objects, and generates a safe draft instead of auto-sending or auto-mutating anything.  
It mirrors the same validation + preview pipeline used in Workflow 1.

---

## 🚀 What This Workflow Does

### 1. Polls Gmail for New Emails
- Runs every X minutes  
- Supports:
  - unread messages  
  - labeled messages  
  - filtered message queries  

### 2. Extracts Structured Fields
- Sender email  
- Subject line  
- Body snippet  
- Message ID  
- Thread info  
- Timestamps  

### 3. Normalizes & Transforms Email Data
- Email cleanup  
- Subject sanitization  
- Body trimming  
- API-ready formatting  
- Converts message into a consistent object shape

### 4. Sends Data to `/validate` and `/dedupe/preview`
- Prevents bad or duplicate records  
- Returns a safe preview diff  
- Never modifies CRM or backend data directly

### 5. Creates a Gmail Draft Instead of Acting Automatically
- Inserts a draft into the user’s Gmail account  
- Draft contains the proposed change or extracted content  
- Perfect for “human-in-the-loop” workflows

---

## 🧱 Nodes Included
- Gmail Trigger (Polling)  
- Set / Code Nodes (Transformations)  
- HTTP Request Nodes (`/validate`, `/dedupe/preview`)  
- Gmail Draft Writer  
- Logging & Retry Blocks  

---

## 🧪 Ideal Use Cases
- Email-to-CRM syncing  
- Support inbox automation  
- Lead enrichment  
- Safe early-stage MVP workflows  
- Human-reviewed processing pipelines  

---

## 📜 License
MIT — reuse and modify freely.

