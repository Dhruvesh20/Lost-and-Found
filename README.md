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
<img width="900" alt="Registration Page" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image1.png" />


# 2️⃣ Email Verification  

The user must open their email inbox and click the Firebase verification link.  
Only after verifying the email can the user click **Register** to complete account creation.  


### 📸 Email Verification Screenshot  
<img width="900" alt="Email Verification 1" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image2.png" />
<img width="900" alt="Email Verification 2" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image3.png" />


# 3️⃣ Dashboard  

After successful registration and email verification, the user is redirected to the **Dashboard**, which provides navigation to all system features:

- Report Lost/Found Item  
- View Lost Items  
- View Found Items  
- My Listings  
- My Responses  

### 📸 Dashboard Screenshot  
<img width="900" alt="Dashboard" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image4.png" />


# 4️⃣ Reporting a Lost or Found Item  

Users can submit an item report via **Report Item**. Required details:

- Item Name  
- Description  
- Verification Question (To authenticate legitimate claimants)  
- Item Type (Lost / Found)  
- Item Image

This ensures accurate identification of reported items.  

### 📸 Report Item Form  
<img width="900" alt="Report Item Form" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image5.png" />


# 5️⃣ My Listings – Reporter-Only Items  

All items reported by the user appear under **My Listings**.

Important behavior:  
- Items in *My Listings* **do NOT appear** in Lost or Found tabs for the same reporting user.  
- Clicking any item shows all responses submitted by claimants/founders.  

### 📸 My Listings  
<img width="900" alt="My Listings" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image6.png" />


# 6️⃣ Lost & Found Tabs (Visible to Other Users)

Other students browsing the system can see reported items categorized as:


### 🔵 Lost Items Tab  
Shows all items marked "Lost" by other users.  

<img width="900" alt="Lost Items Tab" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image7.png" />



### 🟢 Found Items Tab  
Shows items marked "Found" by other users.  

<img width="900" alt="Found Items Tab" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image8.png" />



# 7️⃣ Claiming an Item  

A student can claim an item (lost or found) by:

- Answering the **Verification Question** set by the reporter  
- Uploading a **Proof Image**  

This ensures that only genuine owners or correct founders interact.  

### 📸 Claim Item Form  
<img width="900" alt="Claim Item Form" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image9.png" />


# 8️⃣ My Responses – Track Your Submitted Claims  

Users can view their submitted claims under **My Responses**.

Each response initially has status:

- **Moderation** (Pending Reporter Action)  

### 📸 My Responses Screenshot  
<img width="900" alt="My Responses" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image10.png" />



# 9️⃣ Reporter Moderation – Accept or Reject  

The reporter now reviews responses submitted for their reported item.  
They have two actions:

- **Accept** – If answer matches and proof is valid  
- **Reject** – If the response is invalid  

Accept/Reject controls access to communication.  

### 📸 Moderation Panel Screenshot  
<img width="700" alt="Moderation Panel" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image11.png" />



# 🔟 Chat After Approval  

When the reporter **Accepts** a response:

- Status changes to **Approved**  
- A **Chat Interface** is unlocked for both users  
- They can coordinate retrieval and item handover  

If rejected:
- Status changes to **Rejected**  
- Chat remains disabled  

### 📸 Chat Interface Screenshot  
<img width="900" alt="Chat Interface" src="https://raw.githubusercontent.com/Dhruvesh20/Lost-and-Found/main/assets/images/image12.png" />



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

