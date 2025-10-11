# 📥 Gmail to Google Drive Automation with Zapier

## ⚙️ Overview

In this exercise, you'll learn how to create a simple but powerful automation using **Zapier** that connects **Gmail** and **Google Drive**.

**Objective:** Automatically store email attachments from Gmail in a specific Google Drive folder — but only for emails that meet specific filter conditions (like subject, sender, or label).

---

## 🧠 Learning Goals

- Understand how to use **Zapier** to create automated workflows (Zaps)
- Learn to integrate **Gmail** and **Google Drive**
- Apply filters to control when your Zap should trigger
- Save email attachments to the cloud

---

## 🧰 Prerequisites

Make sure you have the following:

- A **Zapier** account ([sign up here](https://zapier.com/sign-up))
- A **Gmail** account with emails that include attachments
- A **Google Drive** account
- Basic familiarity with Zapier's interface (no coding required)

---

## 🧪 Step-by-Step Lab

### 🔁 Step 1: Create a New Zap

1. Log into [Zapier](https://zapier.com).
2. Click on **Create Zap**.

---

### 📩 Step 2: Set Gmail as the Trigger App

- **App**: Gmail
- **Trigger Event**: `New Attachment`
- Connect your Gmail account
- Choose filters like:
  - Only emails **from** a specific address
  - Only emails **with a specific subject**
  - Or filter by Gmail **Label**

✅ **Tip:** You can fine-tune this trigger using Zapier’s built-in filtering later too.

---

### 🧪 Step 3: Add a Filter (Optional but Recommended)

- **App**: Zapier's built-in **Filter**
- **Condition**: Only continue if...
  - Attachement Details Body Size
  - Exist

---

### ☁️ Step 4: Store the Attachment in Google Drive

- **App**: Google Drive
- **Action Event**: `Upload File`
- Connect your Google Drive account
- Choose the destination **Folder**
- For the **File**, use the attachment object from Gmail

🧠 **Pro Tip:** Use dynamic values like the email subject or date to name your uploaded files.

---

### ✅ Step 5: Test Your Zap

- Send a test email to your Gmail account with an attachment that meets your filter criteria.
- Run the test and check your Google Drive to confirm the upload.

---

### 🚀 Step 6: Turn On Your Zap

Click **Publish** to activate your automation.

---

## 📎 Sample Use Cases

- Automatically back up invoices from a specific supplier
- Save resumes sent to a job application email
- Store research reports or proposals from known contacts

---

## 📘 Resources

- [Zapier Gmail Integration Docs](https://zapier.com/apps/gmail/integrations)
- [Zapier Google Drive Integration Docs](https://zapier.com/apps/google-drive/integrations)
- [Zapier Filter by Zapier Guide](https://help.zapier.com/hc/en-us/articles/8496271886989)

---

## 🙌 Final Thoughts

This no-code automation can save you hours of manual work and reduce human error. It’s a great starting point to explore more advanced Zapier use cases, including multi-step Zaps, branching, and conditional logic.

---

> 🧠 Want more? Try adding a step to send a Slack notification or log the file into a Google Sheet.
