---
id: 20241023122945
created_date: 10/23/2024
updated_date: 10/23/2024
type: note
---

# 📅 Consumer Behavior & Elasticity
- **🏷️Tags** : #10-23-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

## What Do You Think is the Relationship between the Price of These Goods and Services and Consumers' Behavior?
- Prescription eyewear
- Car battery
- Dental care
- Pain medication
- Gasoline 
- Cell phone service
	- How do you think consumers may respond to the changes in price? 
	- How might consumers respond if prices were to go up for cell service and gasoline?
## Price Changes and Consumer Demand
- Price changes affect consumer demand more in some cases than in others. 
- Consumer demand for a product is more or less **elastic** - responsive to changes in price - depending on such factors as how important the product is to the consumer, and how easy or hard it is to find a lower-cost substitute. 

1. **What determines price elasticity of demand?** 
	1. Products that have **substitutes** tend to have a relatively elastic demand. 
	2. Goods and services that take a large portion of the consumer's <b><u>budget</u></b> tend to have an elastic demand (e.g I'll wait to buy that new car) whereas goods and services that take up a small portion of the consumer's budget tend to have an inelastic demand. 
	3. <b><u>Time</u></b>. The more time consumers have to adjust to price changes, the more they will increase purchases in response to price decreases and decrease purchases in response to price increases. Therefore, long-run demand tends to be more elastic than short-run demand. 

### Price Elasticity of Demand
- Price elasticity of demand = `(Q2 - Q1) / [(Q1 + Q2) / 2]` **/** `(P2 - P1) / [(P1 + P2) / 2]`
> ![[price-elasticity-formula-explained-1024x532.webp]]

#### Results...
> **Greater** than 1 = elastic
> **Less** than 1 = inelastic
> **equal to** 1 = unit elastic (equal changes to both)
> (once you complete the calculation, take the absolute Value of the number remaining)

![[Supply_Elasticity_05.png]]![[Elastic-vs.-Inelastic-vs.-Perfectly-Inelastic-Demand.jpg]]![[images.png]]



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