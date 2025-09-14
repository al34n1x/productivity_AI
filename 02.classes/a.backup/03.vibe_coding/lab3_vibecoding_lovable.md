# 🧠 Build a Smart To‑Do App with Lovable AI

This project demonstrates how to create and deploy a full-featured, AI-generated to‑do application using [Lovable AI](https://lovable.so), along with Supabase, Stripe, cloud functions, GitHub integration, and PWA capabilities.

>NOTE: It follows the [DataCamp Lovable AI tutorial](https://www.datacamp.com/tutorial/lovable-ai).



## 📋 What You'll Learn

- How to prototype a full-stack app with Lovable AI
- Integrate Supabase as a real backend
- Add secure user authentication
- Enable daily email reminders with cloud functions
- Restrict features to subscribers with Stripe payments
- Make your app installable as a PWA
- Use GitHub for version control and deployment



## 1. 🚀 Getting Started with Lovable

- Sign up at [Lovable](https://lovable.so) — free tier gives 5 messages per day.
- Type a prompt like:  
  > "I want a simple to‑do list app that lets users add, complete, and delete tasks."

This will generate a React + Vite-based front-end with localStorage support and a UI like this:

![Basic To-Do UI](https://www.datacamp.com/tutorial/lovable-ai/_next/image?url=%2F_to-do-preview.png&w=1080&q=75)



## 2. 🔗 Connect to Supabase

1. Click `Supabase` on the top-right of the Lovable editor.
2. Sign in to [Supabase](https://supabase.com), authorize Lovable.
3. Create a new organization and project.
4. Return to Lovable and select the new project.
5. Lovable updates your code to use Supabase instead of localStorage.




## 3. 🔐 Add User Authentication

Prompt Lovable:

> "Add user authentication so users can log in and only see their own to-dos."

- AI suggests a schema update → Click **Apply Changes**.
- If errors occur, click **Try to fix it**.

The app is now multi-user.



## 4. 📧 Email Reminders via Cloud Functions

Prompt:

> "Send daily email reminders for incomplete tasks."

Steps:
- Lovable sets up a cloud function using cron.
- You'll be asked for a **Resend API key** (use [resend.com](https://resend.com)) to send the emails.
- Lovable will deploy the function and automate email delivery.



## 5. 💰 Add Stripe Subscription Payments

Prompt:

> "Only allow subscribed users to create new tasks."

Steps:
- Lovable generates code to manage Stripe subscriptions.
- You will need to provide your **Stripe API Key**.
- If prompted for a price ID, create a product and price in your [Stripe Dashboard](https://dashboard.stripe.com/products).
- Enter the price ID to complete the integration.

Now, free users will see an upgrade prompt, and paid users can use the full app.



## 6. 📱 Make It a PWA

Prompt:

> "Convert the app into a PWA so it can be installed on mobile."

Lovable automatically adds:
- `manifest.json`
- app icons
- service worker

Your app can now be installed from browser like a native app.



## 7. 🧑‍💻 Connect GitHub & Edit Code

1. In Lovable, go to `Edit Code` → `Connect to GitHub`.
2. Choose your GitHub account/org.
3. The code is pushed to your repo.
4. You can now edit in VS Code or any IDE.
5. Push changes → Return to Lovable → Click **Redeploy**.



## 8. 🚀 Publish Your App

Click **Publish** in the Lovable top bar.

- Copy the public URL to share your app.
- Optionally set a custom domain.
- Any changes pushed to GitHub can be redeployed with a click.




## ⚠️ Notes and Limitations

- **Security**: Lovable configures Supabase but does not enforce security rules. You must manually add Row-Level Security (RLS) to prevent unauthorized access.
- **Developer Experience**: Lovable is great for rapid prototyping but may frustrate experienced devs with limited control.
- **Troubleshooting**: While Lovable can auto-fix most issues, edge cases may require manual edits in code.



## 🧪 Tech Stack

- **Frontend**: React + Vite
- **Backend**: Supabase (PostgreSQL, Auth)
- **Cloud Functions**: Lovable Serverless + Cron + Resend API
- **Payments**: Stripe
- **PWA**: Manifest + Service Worker
- **Versioning**: GitHub
- **Deployment**: Lovable Deploy



## 🛠 Project Setup Summary

```bash
# Install dependencies (optional if modifying locally)
npm install

# Run the app locally
npm run dev

# Make edits via Lovable or GitHub
# Redeploy from Lovable dashboard after pushing

---
[⬅ Back to Course Home](../../README.md)