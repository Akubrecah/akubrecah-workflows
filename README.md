Not a complete readme still under development process 

## 📌 Email Summary to Telegram

## 🔄 What this workflow does
This automation checks your Gmail inbox every minute, detects important emails based on keyword filters, and sends a short, Telegram-style summary using GPT-4o-mini.

---

#### 🧩 Node-by-node Breakdown

1. **📥 Email Received**
   - Gmail Trigger node
   - Polls inbox every minute for new emails (subject + text)

2. **🧪 Is Important**
   - Checks if the email is important using keyword filters.
   - If email subject or body **contains keywords** like `"Sales"`, it continues.
   - Otherwise, it stops.

   **💡 Examples of keywords you can use:**
   - `"invoice"`
   - `"payment due"`
   - `"security alert"`
   - `"job offer"`
   - `"delivery"`  
   👉 Add anything **important to you** in the condition list.

3. **🧠 AI Agent**
   - Sends email content to OpenAI with a pre-written system prompt.
   - Returns a short, human-style summary (max 300 characters) using emojis and plain language.

4. **📤 Send a text message**
   - Sends the AI-generated summary to your Telegram chat.

---

#### ✅ Sample Telegram Message
> 📦 Your Flipkart order “Bluetooth Speaker” was delivered today. Enjoy!

---

#### 🛠 Notes
- You can modify keyword filters in the **Is Important** node.
- Make sure your **Telegram chat ID and bot** are set correctly.
- This workflow works well for:
  - Billing alerts 💰
  - Delivery updates 📦
  - Job or HR emails 🧑‍💼
