# 🚀 Ant UI CRM

A modern **CRM (Customer Relationship Management)** web application built using **React**, **Ant Design**, **Tailwind CSS v4**, and **Vite** — designed for dynamic UI, high performance, and maintainability.  
This project includes authentication, event tracking, member management, reporting, and data export features.

---
<p align="center">
  <img src="https://img.shields.io/badge/React-18.2.0-blue?logo=react" />
  <img src="https://img.shields.io/badge/Vite-5.0-purple?logo=vite" />
  <img src="https://img.shields.io/badge/Ant%20Design-UI-red?logo=antdesign" />
  <img src="https://img.shields.io/badge/TailwindCSS-v4.0-06B6D4?logo=tailwindcss" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>
## 🧱 Tech Stack

- ⚛️ **React** — Component-based UI library
- 🧩 **Ant Design (AntD)** — Enterprise-grade UI components
- 🎨 **Tailwind CSS v4** — Utility-first CSS framework
- ⚡ **Vite** — Next-generation frontend tooling
- 🗄️ **Redux Toolkit** — Simplified state management
- 🔐 **Formik + Yup** — Form handling and validation
- 🌍 **React Router DOM** — Client-side routing
- 📊 **xlsx & jsPDF** — Report and PDF generation
- ⚙️ **Axios** — HTTP client for API requests
- 🧠 **Custom Hooks** — Reusable logic for API and authentication

---

## 📁 Directory Structure

```bash
moorthygithub-ant-ui-crm/
├── README.md
├── eslint.config.js
├── index.html
├── package.json
├── vite.config.js
└── src/
    ├── App.css
    ├── App.jsx
    ├── index.css
    ├── main.jsx
    │
    ├── api/
    │   ├── axios.js
    │   ├── index.js
    │   └── usetoken.js
    │
    ├── components/
    │   ├── AppInitializer.jsx          # Handles environment validation & version check
    │   ├── Layout.jsx                  # Main app layout
    │   ├── Navbar.jsx                  # Top navigation bar
    │   ├── ProtectedLayout.jsx         # Protects private routes
    │   ├── Sidebar.jsx                 # Sidebar navigation with Ant Design menu
    │   ├── VersionCheck.jsx            # Manages app version updates
    │   │
    │   ├── common/
    │   │   ├── AvatarCell.jsx
    │   │   ├── CardHeader.jsx
    │   │   ├── CropImageModal.jsx
    │   │   ├── cropImageUtils.js
    │   │   ├── Logo.jsx
    │   │   └── MaintenancePage.jsx     # Shown during maintenance mode
    │   │
    │   ├── exportExcel/
    │   │   ├── exportEventDetailsReportToExcel.jsx
    │   │   ├── exportEventReportToExcel.jsx
    │   │   ├── exportMemberReportToExcel.jsx
    │   │   ├── exportNotRegisterNotScannedToExcel..jsx
    │   │   └── exportRegisterNotScannedToExcel.jsx
    │   │
    │   ├── json/
    │   │   └── membershipTypes.json
    │   │
    │   ├── MemberList/
    │   │   ├── MemberForm.jsx
    │   │   ├── MemberList.jsx
    │   │   └── MemberTable.jsx
    │   │
    │   ├── pdfExport/
    │   │   └── pdfExport.js
    │   │
    │   ├── STTable/
    │   │   └── STTable.jsx
    │   │
    │   ├── user/
    │   │   ├── ProfileForm.jsx
    │   │   └── UserTable.jsx
    │   │
    │   └── websiteenquiry/
    │       └── WebsiteTable.jsx
    │
    ├── hooks/
    │   ├── useApiMutation.js
    │   └── useLogout.js
    │
    ├── pages/
    │   ├── auth/
    │   │   ├── ForgotPassword.jsx
    │   │   └── SignIn.jsx
    │   │
    │   ├── event/
    │   │   ├── EventAttendMember.jsx
    │   │   ├── EventForm.jsx
    │   │   └── EventList.jsx
    │   │
    │   ├── eventregister/
    │   │   ├── EventRegisterForm.jsx
    │   │   └── EventRegisterList.jsx
    │   │
    │   ├── eventtrack/
    │   │   ├── EventDetailsPage.jsx
    │   │   ├── EventTrackerQR.jsx
    │   │   ├── EventTrackForm.jsx
    │   │   └── EventTrackList.jsx
    │   │
    │   ├── home/
    │   │   └── Dashboard.jsx
    │   │
    │   ├── member/
    │   │   ├── CoupleMembersPage.jsx
    │   │   ├── LifeMembersPage.jsx
    │   │   └── TrusteMemberPage.jsx
    │   │
    │   ├── newRegisteration/
    │   │   ├── NewRegisterationForm.jsx
    │   │   └── NewRegisterationList.jsx
    │   │
    │   ├── profile/
    │   │   ├── ChangePassword.jsx
    │   │   └── Profile.jsx
    │   │
    │   └── report/
    │       ├── EventDetailsReport/
    │       │   ├── EventCard.jsx
    │       │   └── EventDetailsReport.jsx
    │       │
    │       ├── EventReport/
    │       │   └── EventReport.jsx
    │       │
    │       ├── MemberReport/
    │       │   ├── CoupleMemberReport.jsx
    │       │   ├── LifeMemberReport.jsx
    │       │   ├── MemberReport.jsx
    │       │   └── TrusteeMemberReport.jsx
    │       │
    │       ├── NotregisteredNotScanned/
    │       │   └── NotRegisterNotScanned.jsx
    │       │
    │       └── RegisteredNotScanned/
    │           └── RegisteredNotScanned.jsx
    │
    ├── store/
    │   ├── store.js
    │   └── auth/
    │       ├── authSlice.js
    │       ├── companySlice.js
    │       └── versionSlice.js
    │
    └── theme/
        └── AppThemeProvider.jsx
        
---

⚙️ Installation & Setup
1️⃣ Clone the repository (SSH)
git clone git@github.com:moorthygithub/ant-ui-crm.git
cd ant-ui-crm

2️⃣ Install dependencies
npm install

3️⃣ Run the development server
npm run dev

4️⃣ Build for production
npm run build

5️⃣ Preview the production build
npm run preview


🔑 Environment Variables
Create a .env file in the project root with the following keys:
VITE_API_BASE_URL=https://your-api-url.com
VITE_SECRET_KEY=your_secret_key
VITE_SECRET_VALIDATION=your_validation_key


🔐 Authentication Flow


Uses Formik for form handling.


JWT token is stored and validated using a custom hook usetoken.js.


ProtectedLayout.jsx ensures routes are accessible only when authenticated.



🧠 Core Hooks
HookDescriptionuseApiMutation.jsSimplifies API calls (GET, POST, PUT, DELETE).useLogout.jsClears auth data and logs the user out securely.

📊 Reporting & Export
FeatureFileMember Reports/components/exportExcel/exportMemberReportToExcel.jsxEvent Reports/components/exportExcel/exportEventReportToExcel.jsxAttendance Tracking/pages/eventtrack/EventTrackList.jsxPDF Export/components/pdfExport/pdfExport.js

🧩 Reusable Components
ComponentDescriptionSidebar.jsxDynamic Ant Design sidebarNavbar.jsxTop navigation bar with profile menuAppInitializer.jsxValidates environment & handles maintenance redirectionCropImageModal.jsxImage cropper for uploading user photosMaintenancePage.jsxDisplayed when environment fails validation

🎨 Theme Configuration

✨ Implemented via AppThemeProvider.jsx
🌗 Supports both Light & Dark modes
🎨 Integrates Ant Design tokens with Tailwind utilities for cohesive styling

🧰 Development Notes

🌀 Built with Vite for ultra-fast hot module replacement
⚡ Optimized Tailwind via PostCSS
📁 Clean modular folder structure for scalability
💡 Robust error handling for environment validation and version mismatches

📜 License
This project is open-source under the MIT License.

👨‍💻 Author
Moorthy Chandiran
## 📫 Connect with Me
GitHub: https://github.com/moorthygithub
🌐 [Visit My Portfolio](https://moorthyprotfolio.netlify.app/)
💼 [LinkedIn Profile](https://www.linkedin.com/in/moorthy-c-982333217/)


🌟 If you like this project, don’t forget to star the repo!


