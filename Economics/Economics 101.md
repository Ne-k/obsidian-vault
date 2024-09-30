---
id: 20240902092454
created_date: 09/02/2024
updated_date: 09/02/2024
type: note
---

# 📅 Untitled
- **🏷️Tags** : #09-02-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery
Economics is the scientific discipline that studies how societies use scarce resources to produce valuable goods and services, distribute them among individuals, and determine who gets what. The fundamental problem of economics arises from scarcity the fact that human wants are unlimited but our resources (like land, labor, capital) are limited. This leads to three central economic questions: What to produce? How to produce it? And for whom to produce it? Scarcity also implies that every choice we make in the economy involves opportunity costs because allocating any resource to one use means foregoing another potentially beneficial use. Abundance suggests having enough of something so that everyone can have as much as they want; however, true abundance is a theoretical concept since even if one resource becomes abundant, others typically remain scarce. In practical terms, scarcity defines an environment where needs outstrip available resources due to their finite nature and multiple valuable uses.

# 🗒️Notes


## Economics, what is It?
The study of goods and services; production distribution, and consumption of goods and services. 
## Problems
We have unlimited wants and needs

**Scarcity** 
#### Creates 3 Questions
- What to produce? 
- How to produce it? 
- Who to produce for? 
## Scarcity
**Unlimited** wants but **limited** needs 
## Resources
An economic or productive -- required to accomplish an activity 

Unlimited Wants, **Limited** Resources 

---
## Scarcity and Abundance
### Definitions
- A situation in which human wants are **<u>greater than the capacity</u>** of available resources to provide for the wants
- A situation in which a resource has **<u>more than one</u>** valuable use

---
## Opportunity Cost
- Whatever choice you make, you are also giving up something else - Benefits and trade-offs. 
- A tree can make pencils, but you give up making 2x4s.
- Something you lost when you made a choice 

### Definition
- The value of the **Next Best** alternative (essentially the value of the second best choice) 
	- If you use the kayak paddle for firewood, you cannot use it as a fishing rod
	- If you use the drinking water collected from the rain for taking a shower you cannot use it to satisfy your thirst. 
- ...Multiple uses



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
            {"role": "user", "content": f"Give a short summarization of the following notes in a couple sentences: {notes}"}
        ]
    }

    response = requests.post(url, headers=headers, json=data)
    return response.json()

notes = input("Please enter your notes to summarize: ")

summary = summarize_notes(notes)


message_content = summary['choices'][0]['message']['content']
print("Summary:","\n\n" +  message_content)

```