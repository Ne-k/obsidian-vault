---
id: 20241122124100
created_date: 11/22/2024
updated_date: 11/22/2024
type: note
---

# 📅 Aggregate Supply and Demand
- **🏷️Tags** : #11-22-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

## Aggregate Demand (AD)
- The **Aggregate Demand Curve** shows the total amount of goods and services that consumers, businesses, governments and people in other countries will purchase at each and every price level. 
- Represents all the demand in the economy. 
> ![[16f-h 1.png]]

- Why downward sloping? 
	- The Wealth Effect
		-  When the prices fall, people can **buy more with the money they currently have**. 
	- The Interest Rate Effect
		- As **price levels rise**, demand for money rises and **investment spending reduces**. 
	- The Foreign Purchases Effect
		- When price level rises for a good it **becomes more expensive in comparison**. 
		- Decrease in Net Exports.
- Factors causing a shift in the Aggregate Demand Curve are changes in...
	- Consumer Spending
	- Investment Spending
	- Government Spending
	- Net Export Spending 
- **Increases** (LEFT) in AD increase real GDP and the price level. 
- **Decreases** (RIGHT) in AD decrease in real GDP and the price level. 

## Aggregate Supply (AS)

- The **Aggregate Supply Curve** shows the total amounts of goods and services that suppliers will price at each and every price level. 
- A **higher** price level **increases** The quantity of goods and services supplied.
- A **decrease** in the price level decreases the quantity supplied. 
> ![[16g-h 1.png]]

- Anything that **changes production costs** shifts AS.
	- Price inputs
	- productivity
	- Technology
	- Government taxes, subsidies, and regulations.
- **Increases** in AS **increases** real GDP and **lower** price level. 
- **Decreases** in AS **decreases** real GDP and **raise** the price level. 



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
