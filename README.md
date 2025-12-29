# EOD Operator Submission System

This project is a **FREE, serverless EOD (End of Day) submission system** built using **GitHub Pages + Google Apps Script + Google Sheets**.

Operators can submit their EOD data using a simple web form. Operator details are **auto-filled** based on Operator ID, and all data is stored securely in Google Sheets.

---

## 🚀 Features

* ✅ 100% FREE hosting (GitHub Pages)
* ✅ No backend server required
* ✅ Operator ID based auto-fill
* ✅ Conditional fields (Camp / Fixed)
* ✅ EOD period selection (1–5, 6–10, etc.)
* ✅ Data saved directly to Google Sheets
* ✅ Scalable for 100+ operators
* ✅ Mobile & desktop friendly

---

## 🧱 Tech Stack

* **Frontend:** HTML, JavaScript
* **Hosting:** GitHub Pages (Free)
* **Backend API:** Google Apps Script (Free)
* **Database:** Google Sheets
* **File Storage (Optional):** Google Drive

---

## 📂 Project Structure

```
/eod-form
 ├── index.html        # Main EOD form
 ├── README.md         # Project documentation
```

---

## 📊 Google Sheet Structure

### 1️⃣ Operator_Master Sheet

```
Operator_ID | Name | Mode | District | Address
```

### 2️⃣ EOD_Data Sheet

```
Timestamp | EOD_Period | Operator_ID | Name | Mode | District | Address | Camp_Name | File_URL
```

---

## ⚙️ Setup Instructions

### Step 1: Create Google Sheet

* Create a new Google Sheet
* Add two sheets: `Operator_Master` and `EOD_Data`
* Add columns exactly as shown above

---

### Step 2: Create Google Apps Script API

1. Open Google Sheet → **Extensions → Apps Script**
2. Paste the provided `doGet` and `doPost` code
3. Deploy as **Web App**

   * Execute as: **Me**
   * Access: **Anyone**
4. Copy the **Web App URL**

---

### Step 3: Configure Frontend

1. Open `index.html`
2. Replace:

```js
const API = "YOUR_API_URL";
```

with your actual Apps Script Web App URL.

---

### Step 4: Enable GitHub Pages

1. Push files to GitHub repository
2. Go to **Settings → Pages**
3. Source: `main` branch
4. Save

Your site will be live at:

```
https://USERNAME.github.io/eod-form/
```

---

## 🧪 How It Works

1. Operator opens the EOD form link
2. Selects EOD period
3. Enters Operator ID
4. System auto-fills Name, Mode, District, Address
5. Camp Name field appears only if Mode = Camp
6. Operator submits the form
7. Data is stored in Google Sheets

---

## 🔐 Security Notes

* Operator ID validation is mandatory
* Google Sheet access is restricted to admin
* API runs under owner permission
* File size limits can be enforced (if enabled)

---

## 🔧 Optional Enhancements

* 📁 File upload to Google Drive
* 🔒 One EOD per operator per period
* 📊 Dashboard using Looker Studio / Power BI
* 📱 Better mobile UI
* 🔐 OTP / login system

---

## 📌 Use Case

Ideal for:

* CSC / VLE operators
* Field operators
* Daily reporting systems
* EOD / MIS collection

---

## 📞 Support

If you want to extend this system or need customization (dashboard, file upload, validation), you can build on top of this base architecture.

---

**Built with ❤️ using free Google & GitHub tools**
