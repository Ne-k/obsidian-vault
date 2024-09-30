---
id: {{date:YYYYMMDDhhmmss}}
created_date: {{date:MM/DD/YYYY}}
updated_date: {{date:MM/DD/YYYY}}
type: note
---

# 📅 {{title}}
- **🏷️Tags** : #EnglishWarmups

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Warm Ups

Format: 
```
## mm/dd/yy - Title
...
----
```


## 9/11/24 - Padlet Timeline 
### What do these moments (or at least the fact that you chose these moments) reveal about who you are and what kinds of things you value? 
I think the most impactful event on my timeline is probably the Apex Expo event in 2023, as that kind of helped me get out of my comfort zone (a little bit), as I had to talk to students my age as part of my job at the event, and at first I didn't really *like* it, I tried to keep my distance and not let them notice that I was there. But at the event in my free time, when I wasn't in that STEM event, I was helping with the camera interview setup they had in their venue at the expo, and it was where the company I was employed at had set up cameras and recording hardware to interviews employees, CEOs of different electronics companies, and that kind of let me realize that I liked to do multimedia. Another primary event that had an impact on me was the time I got lost in Lego Land, at the time when our group of kids got lost, the older kids didn't know what to do, they didn't have phones, and they essentially just stood around waiting for the parents to come find us - while watching some of the younger kids, and I was (probably) the only kid that had the idea to use a store's phone to call our parents. 

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