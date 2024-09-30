---
id:
  "{ date:YYYYMMDDhhmmss }": 
created_date:
  "{ date:MM/DD/YYYY }": 
updated_date:
  "{ date:MM/DD/YYYY }": 
type: note
Page: "1"
---

# 📅 {{title}}
- **🏷️Tags** : #{{date:MM-DD-YYYY}} #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

## T.S.A And Cinnamon Buns

1. Summarize the story in 3 sentences
	1. The story has a daughter and a father, both going through TSA security, but they got stopped at the TSA checkpoint due to her father's turban on his head due to religion and faith. As the story continues, the narrator starts associating the smell of cinnamon buns to freedom, but her and her father were a minority and an easy target for TSA agents, and her father had to make the decision to comply or not. By the end the agents dismissed them and boarded their plane with buying the daughter a cinnamon bun. 
2. What is a narrative strategy that you thought was well done? (Use figurative language, dialogue, sensory description, hook/ opener, creative sentence structure, etc.) How does this contribute to our understanding of the story? 
	1. The story's structure was well done, jumping straight into the story at the TSA officer questioning her father, and then slowly going into the explanation like how they were a minority and at the same time, adding a 'distraction' with the association of cinnamon buns with freedom, which sounds to be some sort of symbolism to the current situation. 
3. What is the *why* of the story? Identify the takeaway message. How do they *show* this, rather than telling.
	1. The why of the story is that though there is freedom, it comes at some sort of price that isn't as sugary as you might think. They showed this by using the TSA incident as an example, like how at the TSA checkpoint the smell of the cinnamon buns was sweet and sugary, but once they passed the checkpoint the taste "didn't taste as sweet as before."


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