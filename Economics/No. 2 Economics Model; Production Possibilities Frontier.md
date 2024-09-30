---
id: 20240923122245
created_date: 09/23/2024
updated_date: 09/23/2024
type: note
---

# 📅 Economics Model No. 2
- **🏷️Tags** : #09-23-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

### Production Possibilities Frontier and Links and Smiles
#### Production Possibilities
- Economists take into account **alternative ways for utilizing scarce resources**. 
	- The more you produce of one product, the less you will produce in another. 
- **Efficiency**: An economy is using resources in such a way as to <u>maximize the production</u> of goods and services. 
- **Trade-off**: <u>Giving up something</u> that promotes one goal <u>to get more of something</u> that promotes another goal.
- The line on the graph that shows the **maximum possible production**. 
	- Anything **below the frontier** is considered to be **underutilization** because fewer resources are being used than capable.
	- <[Insert Graph]>



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