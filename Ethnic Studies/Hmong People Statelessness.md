---
id: {{date:YYYYMMDDhhmmss}}
created_date: {{date:MM/DD/YYYY}}
updated_date: {{date:MM/DD/YYYY}}
type: note
---

# 📅 {{title}}
- **🏷️Tags** : #{{date:MM-DD-YYYY}} #Notes 

# ✅ Assignments
- [ ]  [Finish Assignment ](https://classroom.google.com/u/2/c/NjkyMDIwOTk1NTMx/m/NzE5NzAyNTEzMTMw/details)

# 🔗 Links
-  [Hmong American Center](https://www.hmongamericancenter.org/hmong-history/)
- [Hmong | History, Culture, and Language - Britannica](https://www.britannica.com/topic/Hmong)
# 💡Summery


# 🗒️Notes

## Hmong American Center

### Life in Laos
- Migrated from southern China in the 19th century to the mountain areas of Laos, Vietnam and Thailand. 
- Worked with the American CIA in the "secret war" in Laos during the Vietnam war 
- Forced to flee their homeland after the victory of the communists. 

### Hmong in Wisconsin

#### Who Are the Hmong
- A group of ethnic people with specific language and culture. 
- <u>Originally came from China with 4,000 years of history</u>
	- Had to leave to Vietnam, Laos, Thailand and Burma at the beginning of the 1800's **due to land expansion by the Chinese government**. 
- Hmong moved out of Laos to seek asylum in European and Western countries after the U.S pulled out of South Vietnam
- There are about **260,000** Hmong Americans living in the US with the majority of them in California, Minnesota, and Wisconsin. 

#### Hmong's Roles with the US during the Vietnam War
- Early 1960's, the US CIA sought out the Hmong and recruited them to fight a "secret war" against North Vietnamese and communist Pathet Lao. 
	- The Hmong people were used to: 
	- harass the communists on Ho Chi Minh Trail 
	- providing intelligence about enemy operations
	- guarding US strategic radar installations
	- and rescuing down American pilots. 
- After the war in 1973, the Hmong were singed out by communist governments of Laos and Vietnam they were: 
	- Hunted down taken to concentration camps
	- Put to hard labor
	- Persecuted 
	- An estimate of 10%, or 35,000 of their population in Laos died as a result
		- many more who suffered with physical, mental, and emotional trauma to this day. 

#### Why Are the Hmong in Wisconsin?
- Hmong are political refugees that **fled their country because of war and persecutions.**
- **Legally admitted to the United States by the government** 
	- initially resettled by church organizations like Catholic Charities and Lutheran Social Service. 
- Some churches sponsored Hmong families in Wisconsin along with other states. 
- By 2010, there were 4**9,240 Hmong Americans living in Wisconsin.** 
- **Milwaukee, Wausau, Sheboygan, La Crosse, Madison, Eau Claire, Appleton, Oshkosh, Manitowoc, Stevens Point, Wisconsin Rapids, Menomonie, and Fond Du La**c are communities that have a significant Hmong population. 
- Hmong people move to Wisconsin to reunite with families, relatives and clan leaders. 
- Wisconsin provides opportunities to Hmong families struggling to create a new life in the United States. 
	- Offers a peaceful and healthy lifestyle 
	- Educational opportunities for both children and adults
	- Agricultural opportunities such as farming and gardening 

#### Hmong Integration in the US
- The Hmong are currently integrating into the American society, making great strides during the past 37 years. 
- 95% of all healthy Hmong-Americans are participating in the local workforce
- Nearly 70% of all Hmong families have become homeowners 
	- and in addition, there is a growing number of Hmong families starting businesses such as: 
		- Grocery stores, 
		- Restaurants, 
		- Specialty stores, 
		-  Small manufacturing companies
- An increasing amount of Hmong high school graduates have gone onto college and universities
	- Many more have graduated from college and are returning to the community to give back to the community to work.
	- Becoming this bridge between the Hmong and the larger communities.  

#### Hmong Involved in Hunting and outdoors

- Traditionally, the Hmong always enjoyed the outdoors
- Hunting and fishing has always been a part of the Hmong's way of life. 
- Thousands on thousands of Hmong are participating in outdoors activities like fishing, and hunting. 
- The Hmong are friendly and respectful people.
	- Will treat others with courtesy and respect 

#### Are the Hmong Coming to the US
- As of right now there are no more Hmong coming to the US
	- The last group of Hmong families that came to the US was between 2004 and 2006
- **The government has no plans on bringing additional Hmong refugees to the country**. 
- In 2009 of December, more than 4,500 refugees in Thailand were returned to Laos
	- There was a fear that the Lao communist government might imprison or even persecute the Hmong leaders and men who were returned 
	- Due to their roles during the Vietnam War 
	- And their resistance against the communist Lao government after the war 

## Hmong | History, Culture, and Language

- Hmong are an ethnic group living in China and Southeast Asia
- Primarily speaking Hmong, one of the Hmong-Mien languages (aka Miao-Yao languages)
- Hmong, among the [Miao](https://www.britannica.com/topic/Miao) groups have slowly migrated out of southern provinces of China
	- Where about 2.7 million still remain.
- Some of the 1.2 million have moved into Vietnam, Laos, Thailand, and eastern parts of Myanmar (Burma). 
- More than 170,000 live in the US
	- Plus 20,000 more in:
		- France (15.000)
		- Australia (2,000)
		- French Guiana (1,500)
		- Canada (600)
		- Argentina (600)
- The Hmong is thought to have been in the Huang He (Yellow River) basin of central China 
- They were slowly driven southward 
- Marginalized by the expanding population of the Han Chinese
- The Hmong practiced the shifting cultivation of unirrigated upland crops; 
	- Buckwheat, 
	- Barley
	- and Millet 

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