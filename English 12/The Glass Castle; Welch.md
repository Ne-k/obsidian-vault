---
id: 20240925083314
created_date: 09/25/2024
updated_date: 09/25/2024
type: note
---

# 📅 The Glass Castle; Welch
- **🏷️Tags** : #09-25-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes




# 🧠 Questions

1. What is the most memorable moment from the story so far? What made this moment memorable? 
	1. The Billy incident, it's just a little too disturbing to not remember, it's like engraved in my head now. 
2. How is life different in Welch than in the desert? 
	1. They aren't moving as much, and one by one, creating a life for themselves. 
3. What do we learn about Rex and Rose through who their parents are/were? How do methods that they were forced to use to cope affect how they raise their own children? 
	1. xx
4. What do you think is going to happen next? 
	1. xx



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