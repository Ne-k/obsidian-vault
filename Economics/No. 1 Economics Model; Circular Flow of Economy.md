---
id: 20240919122728
created_date: 09/19/2024
updated_date: 09/19/2024
type: note
---

# 📅 Untitled
- **🏷️Tags** : #09-19-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes


### Roles in the Economy

- People participate in the economy in may different ways. 
	- <u>Consumers</u>: Buying goods and services
	- <u>Producers</u>: Provide resources to businesses
	- <u>Citizens</u>: Voting on the economic Policy
- "<u>The Invisible Hand</u>" **Vocab**
	- Non verbal
	- A natural phenomenon that guides free markets and capitalism through competition for scarce resources. 

--- 

### Vocabulary: Factors of Production

- **Human Resources (Labor)**: The number of people available for work. 
- **Natural Resource (Land)**: Land that can be used for production. 
- **Capital**: Manufactured or constructed items that businesses use in the production process. 

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