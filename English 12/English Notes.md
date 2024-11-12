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

## Pg. 2

Chronicle of a death foretold pg. 91-95, the effects of Bayardo San Roman
1. What does this section reveal about the events surrounding the crime? 
	- This section delves into Bayardo's psychological state and his reaction to the crime.
	- His demeanor and actions significantly influence the dynamics between the other characters, particularly the Vicario brothers and Angela.
	- Bayardo's reaction can be seen as a catalyst that escalates the events leading up to the murder of Santiago Nasar.
2. What collective illusion does it reveal the community holds? 
	- **Denial and Willful Ignorance:**
	    - Community is aware of the impending crime but fails to prevent it.
	    - Relies on social norms and honor codes to justify their inaction.
	- **Justification through Honor:**
	    - Convince themselves the murder is a matter of honor.
	    - Use this belief to distance themselves from moral responsibility.
	- **Passive Complicity:**
	    - Collective belief enables them to avoid confronting their role in the crime.
	    - Societal pressures and shared delusions lead to tragic outcomes.
	- **Cultural Expectations:**
	    - Community hides behind traditions to absolve guilt.
	    - Façade of cultural norms perpetuates violence and injustice.
1. How does the outcome go against the best interests of the community? 
	- **Loss of Innocence:**
	    - The murder shatters the town's sense of safety and innocence.
	    - People become distrustful and suspicious, altering community dynamics.
	- **Erosion of Moral Integrity:**
	    - Participation in or passive acceptance of the crime erodes the community's moral fabric.
	    - It highlights the weakness in the honor code, questioning the true meaning of justice.
	- **Emotional and Psychological Impact:**
	    - The event leaves lasting emotional and psychological scars on the townspeople.
	    - Guilt and regret permeate the lives of many, leading to long-term mental distress.
	- **Breakdown of Social Trust:**
	    - Trust within the community is compromised, making future cooperation difficult.
	    - The collective failure to prevent the crime fosters an environment of blame and resentment.
	- **Cultural and Social Stagnation:**
	    - The community’s adherence to outdated honor codes prevents social progress.
	    - It reinforces harmful traditions, hindering cultural evolution and growth.
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