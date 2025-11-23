
# Automated Article Generation and Social Media Posting using n8n

**Student Name:** Debajeet Mandal  
**URN:** E25B101817  
**Date of Submission:** 23 November 2025  

---

## 🎯 Aim
To design and implement an automated workflow that generates technology-related articles using **Gemini LLM** and posts them on **LinkedIn** and **Twitter (X)** using **n8n**.

---

## 📘 Introduction

This project focuses on building a fully automated content-generation workflow using **n8n**, capable of:

- Fetching trending tech news  
- Expanding it into a complete article using **Google Gemini LLM**  
- Rewriting and formatting the content for LinkedIn and Twitter  
- Posting automatically using API integrations  

The workflow includes prompt engineering, JavaScript logic, API-based automation, and social media posting — demonstrating real-world automation skills.

---

## 🛠 Tools and Technologies Used

| Tool / Technology | Category | Purpose |
|-------------------|----------|---------|
| **n8n** | Automation Platform | Orchestrates the entire workflow |
| **Gemini LLM** | AI Model | Article generation & rewrite tasks |
| **Cron Trigger** | n8n Node | Schedules daily automation |
| **HTTP Request Node** | API Integration | Fetches trending news |
| **JavaScript Node** | Logic Handling | Random topic selection |
| **Basic LLM Chain** | AI Processing | Article, LinkedIn & Tweet formatting |
| **LinkedIn API** | Social Media | Posts LinkedIn articles |
| **Twitter API (X)** | Social Media | Publishes tweets |

---

## 🗒 Prompts Used

### **A) Article Generation Prompt**
```
You are an expert tech journalist. Write a complete article based on this trending topic.

TITLE: {{$json.title}}
DESCRIPTION: {{$json.description}}

Requirements:
- 100% original
- Easy to read
- Add subheadings
- Add examples
- Add conclusion
```

### **B) LinkedIn Article Prompt**
```
Rewrite this news article for LinkedIn in a professional and insightful way under 2500 characters.

Here is the article: {{ $json.text }}

Just give the final article as output. No extra text.
```

### **C) Twitter Prompt**
```
Rewrite this content as a tweet for Twitter (X):

- Max 280 characters
- Punchy, simple, engaging
- Add relevant trending hashtags

Here is the content: {{ $json.text }}
```

---

## ⚙️ Functionality Overview

| Node | Purpose |
|------|---------|
| **Cron Trigger** | Runs workflow daily at 6 PM IST |
| **HTTP Request** | Fetches trending news (India) |
| **JavaScript Code** | Randomly selects one news topic |
| **LLM (Generate Article)** | Creates full article with structure |
| **Gemini Chat Model** | Powers all LLM tasks |
| **LinkedIn Article Generator** | Professional rewrite |
| **LinkedIn Post Node** | Publishes final article |
| **Tweet Generator (LLM)** | Creates 280-character summary |
| **X Create Tweet Node** | Publishes tweet automatically |

---

## 🔄 Data Flow Summary

**API → JSON → JavaScript → LLM → Re-format → Social Media Posting**

---

## 📚 How the Workflow Operates

1. **Scheduled Trigger**  
   Automatically runs every day at 6:00 PM IST.

2. **Fetch Trending News**  
   HTTP node calls **Newsdata.io API**.

3. **Random Topic Selection**  
   JavaScript picks one random article.

4. **Generate Full Article**  
   Gemini expands it into a complete tech article.

5. **Rewrite for LinkedIn**  
   LLM formats the article professionally.

6. **Post to LinkedIn**  
   via LinkedIn API node.

7. **Summarize for Twitter**  
   Creates a short, punchy tweet with hashtags.

8. **Post to Twitter (X)**  
   via Twitter API node.

---

## ✅ Conclusion

The project successfully automates the entire process of generating and posting tech-related articles using:

- **Newsdata.io API**
- **Google Gemini LLM**
- **LinkedIn API**
- **Twitter API (X)**
- **n8n automation workflow**

This project demonstrates strong skills in **automation design**, **AI content generation**, **API integration**, and **prompt engineering**.

---

## 🙏 Thank You
