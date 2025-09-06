# 🛍️ GenAI-Based Shopping Assistant

## 1. 📌 Overview

**ShopAssist AI** is a smart chatbot that helps users find the perfect laptop. It combines conversational AI (using OpenAI models) with rule-based logic to recommend laptops based on user needs.

---

## 2. ❓ Problem Statement

With so many laptop options online, choosing the right one is hard. ShopAssist AI solves this by chatting with users, understanding their requirements, and suggesting the top 3 best-fit laptops from a dataset.

---

## 3. 💡 How It Works

1. **Conversation**: The assistant asks users questions about what they need in a laptop.
2. **Understanding Needs**: It extracts key preferences like GPU power, portability, display, etc.
3. **Matching**: It compares the user’s needs with a list of laptops and picks the top 3.
4. **Recommendation**: It shares the best matches and continues the conversation to help finalize the choice.

---

## 4. 🧠 What It Understands

The assistant captures 6 key features:

- GPU Intensity
- Display Quality
- Portability
- Multitasking
- Processing Speed
- Budget

Each feature is classified as: `low`, `medium`, or `high` (except Budget which is a number ≥ ₹25,000).

---

## 5. ⚙️ Key Features

- **Chat-Based Interface**  
  Natural, friendly conversation to understand user needs.

- **Safe Input Handling**  
  All inputs checked for safety using OpenAI Moderation API.

- **Smart Recommendations**  
  Uses both AI and rule-based logic to select the best laptops.

- **Laptop Dataset**  
  Laptop info is stored in a CSV file and includes a description, specs, and price.

---

## 6. 🛠️ Main Components

| Function | Purpose |
|---------|---------|
| `initialize_conversation()` | Starts the assistant with a welcome and instructions |
| `moderation_check()` | Flags unsafe user inputs |
| `get_chat_completions()` | Gets responses from the AI model |
| `extract_user_info()` | Builds a profile from user preferences |
| `intent_confirmation_layer()` | Checks if all 6 features are captured correctly |
| `compare_laptops_with_user()` | Matches user profile with laptop data |
| `recommendation_validation()` | Filters top 3 recommendations |
| `initialize_conv_reco()` | Begins the recommendation discussion |

---

## 7. 🖼️ System Flow

```text
User Input ➝ Moderation Check ➝ Intent Extraction ➝ Laptop Matching ➝ Recommendation ➝ Further Chat

