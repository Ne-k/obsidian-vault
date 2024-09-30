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
*At what age were you trusted to practice independence? This could mean being allowed to venture to a friends house beyond our street, go to school on your own either by bus or on foot, going to the store, etc.* 

## Agree/Disagree

1. Safety precautions that most families practice (e.g tracking phones, having babysitters, etc.) are the result of legitimate threads to potential harm to children
	1. Depending on the age, I agree, because if you're at a young age, because you'll obviously worry if your kid will be abducted or not. 
2. Children between the ages of 5-8 should be able to leave the house or complete new tasks without adult supervision. 
	1. Maybe I disagree, because 5-8 is still young for their brains to be developed, at least if you want to experiment, light supervision, like tracking or watching from a corner 
3. Parents should allow children to make mistakes or experience failure
	1. Of course, letting children know what mistakes or failure feels shows them what not to do next time, and to learn from that experience.
4. Children today are less free to practice independence than in previous generations. 
	1. I think children today are given more independence since now parents just give children smart devices at a young age. 

## The 4 Types of Parenting Styles: What Style is Right for You?

1. What does this article believe an idea parenting style is? What does this look like? 
	1. The article recommends authoritative parenting, being strict with the kid and giving them punishments for if they do something wrong makes the kid behave well, eats what everyone else eats, that sort of stuff.
2. What does this article believe to be an harmful parenting style? What does that look like? 
	1. The article thinks that the neglectful parenting style is harmful to the kid, like the parent works long shifts during the day or night, having mental health issues or is a single parent, but the kid tends to overeat and become overweight overtime. 
3. Do you agree with the claims of the article? Why/Why not? 
	1. I think I agree with the article, the parenting styles they describe seem accurate to what I've seen from other families, and I could probably tell what parenting style a person grew up with the longer I interact with that person going off of their personality, lax-ness, etc. 



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