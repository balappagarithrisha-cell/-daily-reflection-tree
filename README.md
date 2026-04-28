# Daily Reflection Decision Tree (Deterministic Model)

## 📌 Overview
This project implements a **deterministic decision tree** for structured daily reflection.  
The goal is to transform vague daily thoughts into **clear, actionable insights**.

Unlike a basic good/bad reflection, this system:
- Uses **emotion-based classification**
- Performs **root cause analysis**
- Maps to **specific actions**
- Produces **consistent outputs**

---

## 🎯 Problem Statement
Daily reflection is often unstructured and inconsistent.  
Users struggle to:
- Identify what actually went wrong or right  
- Convert thoughts into actionable steps  
- Maintain consistency in decision-making  

---

## 💡 Solution Approach
I designed a **step-by-step deterministic decision tree** that:

1. Captures user emotion  
2. Identifies root cause  
3. Maps cause → action  
4. Generates a structured final output  

---

## 🌳 Decision Tree Logic

### Step 1: Mood Identification
User selects:
- Happy  
- Neutral  
- Stressed  

---

### Step 2: Root Cause Analysis

**If Happy:**
- Achievement  
- Positive interaction  
- Personal progress  

**If Neutral:**
- Routine day  
- No significant events  

**If Stressed:**
- Time pressure  
- Distraction  
- External issues  

---

### Step 3: Action Mapping

**Happy →**
- Repeat successful habits  

**Neutral →**
- Introduce one meaningful activity  

**Stressed →**
- Time issue → Create schedule  
- Distraction → Reduce distractions  
- External → Plan backup solutions  

---

### Step 4: Final Output
The system generates:
- Daily Insight  
- Action Plan for Tomorrow  
- Optional Growth Evaluation  

---

## ⚙️ Why This Is Deterministic

This system strictly follows deterministic principles:

- Only **predefined inputs** are allowed  
- Each input leads to a **fixed output path**  
- No randomness or ambiguity  
- Same input always produces the **same result**  

---

## 🛡️ Guardrails (Anti-AI Hallucination)

To ensure reliability:

- Input validation enforced  
- Restricted answer choices  
- No open-ended vague responses  
- Fixed mapping of input → output  

---

## 🤖 Use of AI (Critical Reflection)

### Where AI Helped:
- Brainstorming initial structure  
- Generating base decision tree idea  

### Where AI Was Limited:
- Produced generic and non-deterministic outputs  
- Lacked clarity in structured branching  

### Improvements Made:
- Converted logic into strict deterministic format  
- Added input constraints and validation  
- Designed clear action mapping  
- Removed ambiguity  

---

## 📂 Project Components

- `README.md` → Project explanation  
- `reflection-tree.json` → Structured logic representation  
- `tree-diagram.md` → Visual representation  
- `write-up.md` → Detailed explanation  
- `index.html` → Basic interface (optional enhancement)  
- `transcripts/` → Sample user interaction scenarios  

---

## 🚀 Conclusion

This project demonstrates:
- Structured thinking  
- Deterministic system design  
- Practical problem-solving  

It ensures users can consistently reflect, analyze, and improve their daily decisions with clarity and reliability.
