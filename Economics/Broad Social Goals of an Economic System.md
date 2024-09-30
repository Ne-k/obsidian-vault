---
id: {{date:YYYYMMDDhhmmss}}
created_date: {{date:MM/DD/YYYY}}
updated_date: {{date:MM/DD/YYYY}}
type: note
---

# 📅 {{title}}
- **🏷️Tags** : #{{date:MM-DD-YYYY}} #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

### 1. **Efficiency**
- Refers to how well scarce productive resources are allocated to produce the goods and services people want. 
- How well inputs (resources) are used in the production process to keep production costs as low as possible. 
	- Productive efficiency = fully using all available resources.
	- Allocative efficiency = production represents consumer preferences; marginal benefit = marginal cost. 
### 2. **Equity**
- Means what is **"fair"**
	- Economic actions and policies have to be evaluated in terms of what people think is right and wrong. 
	- Equity issues often arise in questions dealing with the distribution of income and wealth. 
	- Some people judge equity based on providing equal opportunity. 
	- Others judge based on equality of outcomes. 
### 3. **Freedom**
- Refers to such things as: 
	- The freedom for consumers to decide how to spend or save their incomes, 
	- the freedom of workers to change jobs and join unions, and
	- the freedom of individuals to establish new businesses or close old ones.
### 3. **Security**
- Refers to protecting consumers, producers, and resource owners from risks that exist in society. 
	- Each society must decide from which uncertainties individuals can and should be protected, and 
		- whether individuals, 
		- employers, or 
		- the government should provide or pay for this protection.
### 4. **Growth**
- Refers to increasing the production of goods and services over time. 
	- Economic growth is measured by changes in the level of real gross domestic product (GDP). 
	- A target annual growth rate of 3 to 4 % in real GDP has historically been considered to be reasonable and sustainable. 
	- Which raises the questions: 
		- Is it possible for an economy to continually grow? 
		- Is it necessary for an economy to continually grow? 
### 5. **Stability**
- Refers to maintaining stable prices and full employment and keeping economic growth reasonably smooth and ready. 
	- Price stability means avoiding inflation or deflation. 
	- Full employment occurs when an economy's scarce resources, especially labor, are fully utilized. 

# 🧠 Questions

 



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
            {"role": "user", "content": f"Give a short summarization of the following notes in a couple sentences with indentation: {notes}"}
        ]
    }

    response = requests.post(url, headers=headers, json=data)
    return response.json()

notes = input("Please enter your notes to summarize: ")

summary = summarize_notes(notes)


message_content = summary['choices'][0]['message']['content']
print("Summary:","\n\n" +  message_content)

```