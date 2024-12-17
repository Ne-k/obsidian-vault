---
id: 20241209122645
created_date: 12/09/2024
updated_date: 12/09/2024
type: note
---

# 📅 What is Fiscal Policy
- **🏷️Tags** : #12-09-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
- [Notes Slides](https://docs.google.com/presentation/d/1ohex6XgvcaudGT7QFeE3CZ9F2lQkw95MmcFvNJPT9_w/edit#slide=id.p2) 

# 💡Summery


# 🗒️Notes


## What is Fiscal Policy?

- **Fiscal Policy** refers to the government's choices regarding the overall level of government purchases or taxes. 
- Fiscal Policy influences saving, investments, and growth in the long run. 
- In the short run, Fiscal Policy primarily affects the Aggregate Demand. 

## Expansionary Fiscal Policy
- An Increase in government spending and/or a decrease in taxes designed to increase aggregate demand in the economy. The intent is to increase Gross Domestic Product and reduce unemployment. 
> ![[Pasted image 20241209123324.png]]

## Contractionary Fiscal Policy
- A decrease in government spending and/or an increase in taxes designed to decrease aggregate demand in the economy. The purpose is to control inflation. 
> ![[Pasted image 20241209124338.png]]

## Changes in Government Purchases
- When the government alters its own purchases of goods or services, it sifts the aggregate-demand curve directly. 
- There are two macroeconomics effects from the change in government purchases: 
	- The **multiplier** effect: More spending, high waves, leads to more spending.
	- The **Crowding-ou**t effect: Government spending (through loans) increases interest rates leading to private sector spending to decrease because it's more expensive. 
## Changes in Taxes
- When government cuts personal income taxes, it increases households' take-home pay. 
- Households save some of this additional income. 
- Households also spend some of it on consumer goods. 
- Increased household spending shifts the aggregate-demand curve to the right (Positive) 
- The size of the shift in aggregate demand resulting from a low tax change is affected by the multiplier and crowding-out effects. 
- It is also determined by the households' perceptions about the permanency of the tax change. 

## Using Policy to Stabilize the Economy
- Economic stabilization has been an explicit goal of the U.S. policy since the Employment Act of 1946, which sates that: 
	- "It is the continuing policy and responsibility of the federal government to... promote full employment and production."
- The Employment Act has two implications: 
	- The government should avoid being the cause of economic fluctuations. 
	- The government should respond to changes in the private economy in order to stabilize aggregate demand. 



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