---
id: 20241211123051
created_date: 12/11/2024
updated_date: 12/11/2024
type: note
---

# 📅 Fiscal and Monetary Policy
- **🏷️Tags** : #12-11-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

## Monetary Policy
- "The Federal Reserve's actions, as a central bank, to achieve three goals specified by Congress: maximum employment, stable prices, and moderate long-term interest rates in the United States." 

- Tools for Monetary Policy: 
	- 1. Reserve Requirement
	- 2. Interest on Required and Excess Reserves
	- 3. Discount Rate
	- 4. Open Market Operations
## Monetary Policy Tools
- Reserve Requirement: 
	- Banks must keep a percentage of deposits on hand.
	- Raising and lowering the reserve requirement changes the money supply in the economy.
	- ![[Pasted image 20241211124318.png]]
- **Interest on Required and Excess Reserves (PAYYYS!!!)** 
	- Beginning Oct. 1, 2008, the Federal Reserve began paying interest on Bank reserves.
	- If the Fed either raises or lowers interest rates, banks will be compelled to either hold excess reserves or lend them to customers.
	- Increases or decreases the money supply
- ![[Pasted image 20241211125328.png]]
- **Discount Rate (Borrows!!)**
	- Fed = Lender of last resport
	- When banks can't borrow from one another, they borrow from the Federal Reserve
	- Discount Rate = Interest the Fed charges on loans
	- Changing the discount rate signals banks to change their lending activity
	- Impacts the money supply
	- ![[Pasted image 20241211130814.png]]
- 

# 🧠 Questions

# 💬 Recording and Transcription


 

# Summarization Script
```python
import requests

def summarize_notes(notes):
    url = "https://api.pawan.krd/pai-001/v1/chat/completions"
    headers = {
        "Content-Type": "application/json",
        "Authorization": "pk-wBwkkPKdwXKtiUNGWFzhondlUasmPVPQbrDIqZHiUJMXSRUA"
    }
    data = {
        "model": "pai-001",
        "messages": [
            {"role": "assistant", "content": "You are an AI assistant."},
            {"role": "user", "content": f"Give a short summarization of the following notes in 2 sentences with proper indentation: {notes}"}
        ]
    }

    response = requests.post(url, headers=headers, json=data)
    return response.json()

notes = input("Please enter your notes to summarize: ")

summary = summarize_notes(notes)


message_content = summary['choices'][0]['message']['content']
print("Summary:","\n\n" +  message_content)

```