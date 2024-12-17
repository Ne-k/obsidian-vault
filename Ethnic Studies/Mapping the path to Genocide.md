---
id: 20241112104635
created_date: 11/12/2024
updated_date: 11/12/2024
type: note
---

# 📅 Mapping the Path to Genocide
- **🏷️Tags** : #11-12-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

## "A Genocide Begins with the Killing of One Man - not for what He Has Done, but because of Who He is."

Quote Reflection: 

--- 

## What is Genocide?
- The "Ten Stages of Genocide" is a formula for how a society can engage in genocide. <u>Genocide cannot be committed by an individual or small group; rather, it takes the cooperation of a large number of people and the state.</u> The genocidal process starts with prejudice that continues to grow. By knowing the stages of genocide, citizens are better equipped to identify the warning signs and stop the process from continuing.  
- How would you <u>define</u> "genocide"? 
	- A deliberate killing of a group of a minority with the aim of destroying them, like the holocaust. 
### The Most Commonly Cited Semination for Genocide is the Legal Definition as Set out by the United Nations Convention on the Prevention and Punishment of the Crime of Genocide (1948):

> Genocide" means any of the following acts committed with **intent to destroy**, in whole or in part, a national, ethnical, racial or religious group, as such:
	(a). **Killing** members of the group; 
	(b). Causing serious **bodily or mental** harm to members of the group; 
	(c). Deliberately inflicting on the group **conditions of life** calculated to bring about its **physical destruction** in whole or in part; 
	(d). Imposing measures intended to **prevent births** within the group; 
	(e). Forcibly **transferring children** of the group to another group. 

## Ten Stages of Genocide

1. **Classification** is something that all societies have. IT is a way to divide societies into different groups and distinguish between "us" and "them". Bipolar societies (that are divided into only two major groups) are more likely to experience genocide. 
2. **Symbolism** is the characterized by naming different groups or distinguishing them through symbols, colors, or dress. This happens everywhere and is not necessarily negative unless it is combined with hatred, which can lead to discrimination or dehumanization. 
3. **Dehumanization** occurs when one group denies the humanity of another group. As part of this process, people are commonly called insects, vermin, or diseases. By first dehumanizing victims, the general public may be less shocked by mass murder, because they do not view the victims as fully human. At this stage, propaganda including newspapers, television, ratio and social media could be used to ferment represent against the targeted group. 
4. **Organization** happens when perpetrators create a plan for genocide and train and arm militias. Those in charge may set up secret police to spy on, attest, torture, and murder people suspected of being in opposition to the regime or to the genocide. 
5. **Polarization** occurs when moderate leaders and groups are eliminated, leaving a polarized society. At this point, propaganda is more widespread laws may be created to keep people from marrying into other groups, and often emergency decrees are announced in order to "protect the nation." 
6. **Preparation** is the process of preparing for mass murder. Leaders use euphemisms to hide their intentions ("purification", "relocation", or "counter terrorism" ). Propaganda about the victimized group(s) continues to be promoted and armies are given weapons and training. 
7. **Persecution** occurs when victims are identified and separated from society. For example victims are sometimes forced into living in ghettos. Leaders of the genocide draw up lists of people or communities targeted for death and deprive their victims of basic resources like water and food. Violent acts often begin at this stage. 
8. **Extermination** is the mass killing we know as genocide. The term 'extermination' usually refers to the killing of insects and vermin; in the context of genocide, this term is used to further dehumanize victims. 
9. **Denial** is the final stage of genocide and it takes many forms. In some cases perpetrators attempt to cover up the evidence. In other cases, they deny that any crimes were committed or minimize the number of people killed. Denial often begins during the extermination and can last long after the genocide, continuing harm for generations.  


## The Holocaust


| Important Dates        | - January 30 1993<br>- March 20 1933<br>- April 1 1933<br>- September 15 1935<br>-November 9-10 1938            |     |
| ---------------------- | --------------------------------------------------------------------------------------------------------------- | --- |
| Location               | - Germany camps<br>- Poland<br>- Netherland<br>- France<br>- Hungary<br>- Soviet Union                          |     |
| Causes                 | - Antisemitism<br>- Nazi ideology<br>- economic instability<br>- nationalism<br>- propaganda and indoctrination |     |
| Key Points             | - Adolf Hitler's rise to power in 1933<br>- Nuremberg Laws<br>                                                  |     |
| Consequences           |                                                                                                                 |     |
| International Response |                                                                                                                 |     |
> -> **Video Reflection**, <u>The Holocaust</u>: What were the factors that enabled such a large-scale genocide  like the Holocaust to occur, and how did the Nazis manipulate public opinion to promote hatred? 
> Reflect on how we can learn from this tragic history to prevent similar atrocities in the future.  
- The idea that some people are less than others
- Genocide begins and ends with people's choices
- They manipulated film and news, stifled the press to spread hate speech of minorities 
- The spread of propaganda 

## Cambodian Genocide

| Important Dates        |     |
| ---------------------- | --- |
| Location               |     |
| Causes                 |     |
| Key points             |     |
| Consequences           |     |
| International Response |     |


# 🧠 Questions

# 💬 Recording and Transcription


 

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