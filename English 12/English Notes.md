---
id: 20241015090136
created_date: 10/15/2024
updated_date: 10/15/2024
type: note
---

# 📅 English Notes
- **🏷️Tags** : #10-15-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

### Pg. 1
- How would you identify an ideal parent? What kind of parent would you want to be? Do your parents adhere to your definition? 
	- I think someone who is moderate strict but also give their kids some form of freedom, like not too much or too little, because too much freedom their kid won't understand rules, while too little freedom their kids will be a rule listener but won't have the sense of themself. I think my parents follow that idea. 
- How important is consistency and routine? Do we need routine in order to create cleaner pathways to find success, or is it more important to lean with disarray and uncertainty? 
	- While the kid is young, I think a semi-consistent routine is viable to create a cleaner pathway for success, but occasionally deviate from it to teach the kid what is orderly or disorderly. 



# 🧠 Questions

# Recording and Transcription


 

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