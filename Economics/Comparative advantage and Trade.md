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

- **Absolute Advantage**: The ability to <u>produce more units of a good or service than some other producer</u> using 
- **Comparative Advantage**: 
- Comparative advantage is the <u>economic basis for specialization and trade</u>
- If countries specialize in producing the goods in which <u>they have the comparative advantage and trade for the goods in which others have the comparative advantage</u>, both parties will be <u>better off</u>.

- Specialization relates to higher standard of living 
- Efficiency and productivity 
### Comparative
- A person or nation can produce something most efficiently 
- The circumstance in which a country gives up something less or lower opportunity cost. 
- Each person should produce the good that has the lower opportunity cost than competitors

### Absolute
- Time is a limited resource 


#### **Interdependence**
- The shared need of countries for the resources, goods services, labor 



**US**: 20 Planes **(1P costs 1/10C)**, 2 Cruise Ships (**1C costs 10P**)
**France**: 12 Planes (**1P costs 1/6C**, 2 Cruise Ships (**1C costs 6P**)

> The US Should create planes, France should make Cruise Ships because of the lower opportunity cost. 
> 
> France has a lower opportunity cost at 6 Planes, and the US has a lower opportunity cost at 1/10 Cruise Ships
### **COST** (Of What You're producing) / **GAIN** (What You Get back)

#### A Country Cannot Have a Comparative Advantage in both Categories

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