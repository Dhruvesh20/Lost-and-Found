# 🏫 Lost & Found Portal – College Lost & Found Management System

The **Lost & Found Portal** is a web-based application designed to streamline the process of reporting, tracking, and recovering lost or found belongings within a college campus. It provides a clean and secure way for students to register, authenticate, report items, claim items, verify claims, and communicate through an integrated chat module.

This README explains the complete working of the application **step by step with screenshot sections**.


# 🚀 Project Overview

**Project Name:** Lost & Found Portal  
**Target Users:** College Students  
**Purpose:** Digitize and simplify the lost and found process on campus  


# 🧰 Technologies Used

| Feature | Technology |
|--------|------------|
| Frontend | React |
| Backend Logic | JavaScript |
| Authentication | Firebase Email Verification |
| Email Notifications | Resend (Welcome Emails Implemented) |
| Image Storage | Supabase Buckets |


# 📝 Step-By-Step Functional Explanation (With Screenshot Sections)

# 1️⃣ User Registration

A student begins by registering using the following details:  
- Full Name  
- Student ID  
- Email  
- Branch  
- Password  

After filling the form, the user clicks **Send Link**, which triggers Firebase to send a verification link to the provided email.  

### 📸 Registration Page  
<img width="975" height="459" alt="image" src="https://github.com/user-attachments/assets/a9b878cf-6183-465f-875d-5ae337e9df1c" />


# 2️⃣ Email Verification  

The user must open their email inbox and click the Firebase verification link.  
Only after verifying the email can the user click **Register** to complete account creation.  


### 📸 Email Verification Screenshot  
<img width="1517" height="235" alt="image" src="https://github.com/user-attachments/assets/b08e5529-7884-425d-8664-36fc807fb9c6" />
<img width="1541" height="678" alt="image" src="https://github.com/user-attachments/assets/37fdc2be-ca76-47ea-999a-694de3cd73f5" />


# 3️⃣ Dashboard  

After successful registration and email verification, the user is redirected to the **Dashboard**, which provides navigation to all system features:

- Report Lost/Found Item  
- View Lost Items  
- View Found Items  
- My Listings  
- My Responses  

### 📸 Dashboard Screenshot  
<img width="975" height="461" alt="image" src="https://github.com/user-attachments/assets/b9d7b71e-fdb6-49e9-b1ec-1cdd04ce9819" />


# 4️⃣ Reporting a Lost or Found Item  

Users can submit an item report via **Report Item**. Required details:

- Item Name  
- Description  
- Verification Question (To authenticate legitimate claimants)  
- Item Type (Lost / Found)  
- Item Image

This ensures accurate identification of reported items.  

### 📸 Report Item Form  
<img width="975" height="467" alt="image" src="https://github.com/user-attachments/assets/38720a32-f0dc-4dde-8796-2fbca65cc557" />


# 5️⃣ My Listings – Reporter-Only Items  

All items reported by the user appear under **My Listings**.

Important behavior:  
- Items in *My Listings* **do NOT appear** in Lost or Found tabs for the same reporting user.  
- Clicking any item shows all responses submitted by claimants/founders.  

### 📸 My Listings  
<img width="975" height="390" alt="image" src="https://github.com/user-attachments/assets/31bc4714-d7f0-40bd-8489-95e6e1daa738" />


# 6️⃣ Lost & Found Tabs (Visible to Other Users)

Other students browsing the system can see reported items categorized as:


### 🔵 Lost Items Tab  
Shows all items marked "Lost" by other users.  

<img width="975" height="338" alt="image" src="https://github.com/user-attachments/assets/ee21a601-7bf6-4c84-9a72-99c2d3679bf5" />



### 🟢 Found Items Tab  
Shows items marked "Found" by other users.  

<img width="975" height="334" alt="image" src="https://github.com/user-attachments/assets/60e42555-4a62-4798-8ecc-2216bd3733e3" />



# 7️⃣ Claiming an Item  

A student can claim an item (lost or found) by:

- Answering the **Verification Question** set by the reporter  
- Uploading a **Proof Image**  

This ensures that only genuine owners or correct founders interact.  

### 📸 Claim Item Form  
<img width="975" height="457" alt="image" src="https://github.com/user-attachments/assets/afbc2f9b-fa90-4174-8519-29ffa8c3003d" />


# 8️⃣ My Responses – Track Your Submitted Claims  

Users can view their submitted claims under **My Responses**.

Each response initially has status:

- **Moderation** (Pending Reporter Action)  

### 📸 My Responses Screenshot  
<img width="975" height="335" alt="image" src="https://github.com/user-attachments/assets/a899a655-630b-4ba4-9997-f20d41f2078a" />



# 9️⃣ Reporter Moderation – Accept or Reject  

The reporter now reviews responses submitted for their reported item.  
They have two actions:

- **Accept** – If answer matches and proof is valid  
- **Reject** – If the response is invalid  

Accept/Reject controls access to communication.  

### 📸 Moderation Panel Screenshot  
<img width="763" height="591" alt="image" src="https://github.com/user-attachments/assets/548a22c9-b3ab-4435-9b29-456dd55b7b42" />



# 🔟 Chat After Approval  

When the reporter **Accepts** a response:

- Status changes to **Approved**  
- A **Chat Interface** is unlocked for both users  
- They can coordinate retrieval and item handover  

If rejected:
- Status changes to **Rejected**  
- Chat remains disabled  

### 📸 Chat Interface Screenshot  
<img width="975" height="400" alt="image" src="https://github.com/user-attachments/assets/340a9f89-f6a4-4942-986c-ad9b9cf1603b" />



# 🎯 User Roles Summary

| Role | Permissions |
|------|-------------|
| **Reporter** | Report items, review claims, approve/reject responses, chat on approval |
| **Claimant** | Submit claim, view claim status, chat after approval |
| **Founder** | Report found items, verify ownership, submit proof, chat after approval |


# 📬 Email Notifications (Resend)

Currently implemented:  
- **Welcome Email** sent automatically upon registration  

Future scope may include email notifications for:  
- Status changes (Approved/Rejected)  
- New Responses  
- Chat Message Alerts  


# 🗃 Supabase Storage

Used for storing:
- Item images  
- Claim proof images  

Offers secure, CDN-backed file delivery.


# 🔐 Firebase Authentication

Used for:
- Sending verification emails  
- Ensuring only verified student accounts can register  
- Securing user sessions  

Prevents unauthorized activity and keeps the platform student-exclusive.

# 🎉 Final Summary

The Lost & Found Portal offers a complete digital workflow for lost item recovery in a college campus environment:

- Secure User Registration  
- Verified Access  
- Robust Reporting System  
- Public Lost/Found Visibility  
- Claim & Proof Mechanism  
- Reporter Moderation  
- Real-Time Chat After Approval  

This ensures a safe, transparent, and efficient process for item restoration.

# 🔗 Website Link

**Live Website:** https://kjsitlaf.vercel.app/

