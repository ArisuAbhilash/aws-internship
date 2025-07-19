<p align="center">
  <img src="screenshots/sns-logo.png" width="120"/>
</p>

<h1 align="center" style="color:#2E86C1;">AWS SNS – Simple Notification Service Guide</h1>
</br>

<h3 align="left" style="color:#2E86C1;">📝 Introduction</h3>

---

**Amazon Simple Notification Service (SNS)** is a **fully managed messaging service** used to send:

- **SMS (Text Messages)**
- **Emails**
- **Push Notifications**
- **Messages to HTTP/HTTPS endpoints**
- **Messages to AWS Lambda functions or SQS queues**

It is commonly used for **alerts, notifications, and system-to-system messaging**.

---

<h3 align="left" style="color:#2E86C1;">📦 SNS Messaging Types</h3>

---

### ✅ **1️⃣ A2P – Application to Person**

- Sends **notifications from applications to people**  
- **Common Uses:**
  - SMS alerts  
  - Email notifications  
  - OTP verifications  
- **Example in this guide:** Sending SMS from AWS SNS to your mobile phone.

---

### ✅ **2️⃣ A2A – Application to Application**

- Sends **messages between systems or services**  
- **Common Uses:**
  - Triggering AWS Lambda  
  - Sending data to SQS queues  
  - Webhooks to HTTP/HTTPS endpoints  
- **Example Use Case:** Triggering an event-driven workflow in AWS.

---

### 🔍 **Summary Table**

| **Type** | **Purpose** | **Example** |
|----------|-------------|-------------|
| **A2P** | Notify people | SMS, Email |
| **A2A** | Notify applications | Lambda, SQS, HTTP |

---

<h3 align="left" style="color:#2E86C1;">🧭 Step-by-Step SNS Setup</h3>

---

### 📌 **Step 1: Open SNS in AWS Console**

- Go to **AWS Console**
- In the **search bar**, type **SNS** and select **Simple Notification Service**

---

### 📌 **Step 2: Create a Topic**

- Click on **Create Topic**
- **Select Topic Type:**  
  - **Standard** (For SMS & Email)  
  - **FIFO** (For strict message ordering – not used here)

#### **For this guide, select:**  
`Standard Topic`

- **Topic Name:** Example: `my-alerts-topic`  
- **Display Name (for SMS):** Example: `MyAlerts`

---

### 📌 **Step 3: Finalize Topic Creation**

- Skip optional settings or configure them as per need  
- Click **Create Topic**

---

### 📌 **Step 4: Create a Subscription**

- Click on your **created Topic**
- Select **Create Subscription**

#### **Subscription Settings:**

- **Topic ARN:** Auto-selected  
- **Protocol:** `SMS` (for text messages)

---

### 📌 **Step 5: Add Sandbox Phone Number**

Since AWS SMS requires verification:

1. Go to **Sandbox → Phone numbers**  
2. Click **Add Phone Number**  
3. Enter your phone number  
4. You will receive an **OTP (One-Time Password)**  
5. Enter the OTP and **Confirm**

---

### 📌 **Step 6: Complete Subscription**

- After verifying the number, **go back to Create Subscription**  
- Select the **verified phone number**  
- Click **Create Subscription**

---

### 📌 **Step 7: Publish a Message**

- Go to your **SNS Topic**  
- Click **Publish Message**

#### **Fill the form:**

- **Subject:** Any title (Example: `Alert!`)  
- **Message ID:** Random numbers (auto-generated or enter manually)  
- **Message Body:** Your message content (Example: `Server CPU usage is high!`)

Click **Publish**

---

<h3 align="left" style="color:#2E86C1;">✅ Final Output</h3>

---

- Check your **mobile phone**.  
- You will receive the **SMS notification** from AWS SNS.

---

<h3 align="left" style="color:#2E86C1;">📽️ Video Demonstration</h3>

---

> Watch the **complete SNS setup video** for better understanding.

<p align="center">
  <a href="https://drive.google.com/file/d/1qO1nGuZszL4_VfaJzYPK5iNOgzRukJXN/view?usp=drive_link">
    <img src="screenshots/sns-video-thumbnail.png" width="600" alt="Watch Video"/>
  </a>
</p>

---

<h3 align="left" style="color:#2E86C1;">📚 Learnings</h3>

---

- Difference between **A2P and A2A messaging**  
- How to create a **Standard SNS Topic**  
- How to **verify phone numbers** (Sandbox Mode)  
- How to **send SMS notifications** using SNS

---

## 🔗 Resources

- [AWS SNS Documentation](https://docs.aws.amazon.com/sns/latest/dg/welcome.html)  
- [AWS Free Tier](https://aws.amazon.com/free)

