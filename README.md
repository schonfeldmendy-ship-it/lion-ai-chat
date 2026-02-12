# Lion AI Chatbot Deployment Guide

## 1. Get Your Free API Key
1. Go to [Google AI Studio](https://aistudio.google.com/).
2. Create a new API key.
3. Save it for later.

## 2. Deploy the Backend to Vercel (Free)
This API handles the conversation securely.

1. **Create a GitHub Repository:**
   - Create a new repository on GitHub (e.g., `lion-ai-chat`).
   - Upload the files (`api/`, `package.json`) to it.

2. **Deploy on Vercel:**
   - Go to [Vercel.com](https://vercel.com/) and sign up/login.
   - Click "Add New..." -> "Project".
   - Import your GitHub repository.
   - In the "Environment Variables" section, add:
     - Key: `GEMINI_API_KEY`
     - Value: (Paste your Google AI Studio key here)
   - Click **Deploy**.

3. **Get Your Backend URL:**
   - Once deployed, copy the domain (e.g., `https://lion-ai-chat.vercel.app`).

## 3. Embed on Google Sites
Now you will add the chat interface to your site.

1. Open `public/index.html` on your computer.
2. Find the line: `const API_URL = "YOUR_VERCEL_URL/api/chat";`
3. Replace `YOUR_VERCEL_URL` with your actual Vercel domain (e.g., `https://lion-ai-chat.vercel.app/api/chat`).
4. Copy the **entire content** of the file (HTML, CSS, and JS).
5. Go to your Google Sites editor.
6. **Option A (Dedicated Chat Page - Recommended):**
   - Create a new page named "Lion AI Chat".
   - Click **Insert** -> **Embed** -> **Embed Code**.
   - Paste the code.
   - Resize the embed to fill the screen or a large central area.
7. **Option B (Widget on Contact Page):**
   - Go to your Contact Us page.
   - Click **Embed Code**.
   - Paste the code.
   - Resize the box to be tall enough (approx 600px height, 400px width) so the chat window fits when open.
   - *Note:* In Google Sites, "floating" widgets stay inside their box, so make the box big enough!

## Testing
- Open your site.
- Type a message like "What are the top threats in 2026?"
- Lion AI should respond with the specific list from your requirements.
