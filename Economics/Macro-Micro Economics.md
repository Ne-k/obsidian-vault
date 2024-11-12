---
id: 20241107125257
created_date: 11/07/2024
updated_date: 11/07/2024
type: note
---

# 📅 Macro/Micro Economics
- **🏷️Tags** : #11-07-2024 #Notes 

# ✅ Assignments
- [ ]  

# 🔗 Links
-

# 💡Summery


# 🗒️Notes

> How do we measure a nation's...

## 1. Measure a Nation's Income

> **Microeconomics** is the study of how individual households and firms make decisions and how they interact with one another in markets. 

> **Macroeconomics** is the stud of the economy as a whole. Its goal is it explain the economic changes that affect many households, firms, and markets at once. 

**Macroeconomics** answers questions like the following: 
- Why is the average income high in some countries and low in others? 
- Why do prices rise rapidly in some time periods while they are more stable in others? 
- Why do production and employment expand in some years and contract in others? 

## 2. The Measurement of Gross Domestic Product
- **Gross domestic product** (GDP) is a measure of the income or expenditures of an economy. 
- GDP is the total market value of all final goods and services produced within a country in a given period of time...
- "GDP is the market value..." 
	- Output is values at market prices. 
- "... Of All..." 
	- Includes all items produced in the economy and legally sold in markets. 
- "... Final..."
	- It records only the value of final goods, not intermediate goods (the Value is counted only once).   
- "... Goods and Services..." 
	- That includes both tangible goods (food, clothing, cars) and intangible services (haircuts, housecleaning, doctor visits). 
- "... Produced..." 
	- It includes goods and services currently produced, not transactions involving goods produced in the past. 
- "... Within a country..." 
	- It measures the value of production within the geographic confines of a country. 
- "... In a Given Period of Time..." 
	- It measures the value of production that takes place within a specific interval of time, usually a year or a quarter (three moths). 

## 3. The Components of GDP
- GDP includes all items produced in the economy and sold legally in markets.
- What is Not Counted in GDP?
	- GDP excludes most items that are produced and consumed at home and that never enter the marketplace. 
	- It excludes items produced and sold illicitly, such as illegal drugs. 
--- 
- Consumption (C)
	- The spending by households on goods and services, with the exception of purchases of new housing. 
- Investment (I)
	- The spending on capital equipment, inventories, and structures, including new housing. 
- Government Purchases (G) 
	- The spending on goods and services by local, state, and federal governments.
	- Does not include transfer payments because they are not made in exchange for currently produced goods or services. 
- Net Exports (NX) 
	- Exports minus imports. 
### **Y = C + I + G + NX**

## 4. Real Versus Nominal GDP
- **Nominal GDP** values the production of goods and services at *current prices*. 
- **Real GDP** values the production of goods and services at *constant prices*
- GDP Deflator (Index #) 
	- = <u>Nominal GDP</u> * 100 
	- Real GDP
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