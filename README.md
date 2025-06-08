# 🧠 Ask Samuel – AI Portfolio Chatbot

A simple, interactive chatbot that showcases your skills and experience, built with **Streamlit**.
✅ Clean UI
✅ Responds to questions about your tech stack
✅ Deployable for **free** in under 10 minutes

---
✅ By the time you are done! Your chatbot will be live on a `streamlit.app` link like:

```
https://app.snowflake.com/me-central2.gcp/ns67402/#/streamlit-apps/MYCHATBOT.PUBLIC.LDH2IEIT3XZQ6QVW?ref=snowsight_shared
```


## ⚙️ Tech Stack

* **Python** (Backend Logic)
* **Streamlit** (Frontend UI)
* **GitHub** (Code hosting)
* **Streamlit Cloud** (Deployment)

---

## ✅ 1. Prerequisites

Before you begin, make sure you have:

* **Python 3.8+** installed → [Download Python](https://www.python.org/downloads/)
* **pip** installed (usually comes with Python)

---

## 📁 2. Project Setup

### 👉 Step-by-Step

#### A. Create Folder

```bash
mkdir ask-samuel-chatbot
cd ask-samuel-chatbot
```

#### B. Create `main.py`

Paste this code below inside `main.py`:

```python
import streamlit as st

st.set_page_config(page_title="Ask Samuel - Chatbot Portfolio", layout="centered")

# Title and intro
st.title("🤖 Ask Samuel")
st.subheader("Interactive Chatbot Portfolio")
st.markdown("""
Welcome! I'm **Samuel**, an AI Solutions Specialist with a passion for building smart, scalable, and creative tools.  
This chatbot is a quick, interactive way to learn more about my work. Ask me anything from the suggestions below!
""")

# --- Predefined Q&A Data ---
qa_data = {
    "what are your skills?": "I specialize in AI tools, chatbot development, API integration, LMS design, and avatar-based systems. I’m skilled in backend engineering, fast prototyping, and building systems that scale using modern tools and clean code practices.",
    "what programming languages do you know?": "My primary language is Python, but I'm also experienced with JavaScript, HTML/CSS, SQL, and have working knowledge of PHP, Node.js, and basic Java for logic implementation.",
    "have you worked with ai avatars?": "Yes, I’ve built avatar-based onboarding and training demos using platforms like D-ID and Synthesia. I also know how to script dynamic avatar behavior and integrate them into LMS flows or websites.",
    "can you build a learning management system?": "Absolutely. I've contributed to LMS development with features like user role control, AI chatbot tutors, auto-grading, and video training delivery. I use Django, Streamlit, Firebase, and even Notion-like UIs depending on scope and scale.",
    "where can i see your projects?": "Check out my GitHub: [github.com/scriptedSyntax](https://github.com/scriptedSyntax) and my YouTube demos: [youtube.com/@SamPlifiedBytes](https://www.youtube.com/@SamPlifiedBytes)",
    "tell me about your experience.": "I’ve worked on SaaS platforms, built AI prototypes under tight deadlines, and integrated APIs across healthcare, education, and e-commerce sectors.",
    "what are your top tools?": "Python, Django, Streamlit, D-ID, OpenAI API, LangChain, GitHub, Postman, Firebase, and Google Colab. Also familiar with Bootstrap, Tailwind, and basic React.",
    "can i hire you?": "That’s why I built this! I'm ready to work, fast on delivery, and open to long-term or project-based roles. Let’s connect — I’m here to help drive your AI and automation goals forward."
}

sample_questions = list(qa_data.keys())

# Normalize questions (case-insensitive matching)
def normalize(text):
    return text.strip().lower()

# Chat interface
user_input = st.text_input("💬 Ask a question about Samuel...")

if user_input:
    key = normalize(user_input)
    response = qa_data.get(key, None)

    if response:
        st.markdown(f"**Samuel Bot:** {response}")
    else:
        st.warning("🤔 I’m not sure how to answer that yet. Try asking one of the following:")
        for q in sample_questions:
            st.markdown(f"- **{q.capitalize()}**")

# Optional static sample questions below input
st.markdown("### 📌 Sample questions you can ask:")
for q in sample_questions:
    st.markdown(f"- {q.capitalize()}")
```

#### C. Create `requirements.txt`

Paste this inside a new file called `requirements.txt`:

```
streamlit
```

---

## 🧪 3. Test Locally

Open a terminal and run:

```bash
pip install -r requirements.txt
streamlit run main.py
```

👉 The app will open in your browser at `http://localhost:8501`

---

## 🚀 4. Deploy for Free (Streamlit Cloud)

### A. Push to GitHub

1. Create a **new public GitHub repo** (name it `ask-samuel-chatbot`)
2. Push your files:

```bash
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/ask-samuel-chatbot.git
git push -u origin main
```

### B. Deploy on Streamlit Cloud

1. Go to [streamlit.io/cloud](https://streamlit.io/cloud)
2. Click **“Deploy an App”**
3. Connect your GitHub → Select your repo
4. Set the entry point to `main.py`
5. Click **Deploy**

✅ Done! Your chatbot will be live on a `streamlit.app` link like:

```
https://app.snowflake.com/me-central2.gcp/ns67402/#/streamlit-apps/MYCHATBOT.PUBLIC.LDH2IEIT3XZQ6QVW?ref=snowsight_shared
```
