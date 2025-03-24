# **AI Worksite Manager**  
A **custom ServiceNow application** built using **ServiceNow Studio**, designed to efficiently manage **AI-powered devices **. This application enables **seamless tracking of AI devices**, **request management**, **automated workflows**, **custom UI enhancements**, **role-based access control**, and **notification mechanisms** to improve operational efficiency.

---

## **📌 Key Functionalities & Features**  

### **1️⃣ Data Model & Database Structure**  
The application is built on a structured **data model** that ensures efficient data management and retrieval.  

#### **📂 Custom Tables**  
- **AI Devices (`x_1425035_ai_works_ai_devices`)**  
  - Stores details of AI-powered devices available in the worksite.  
  - Attributes include **Device Name, Type, Model, Status, Assigned User, Location, Last Service Date, etc.**  

- **Device Request (`x_1425035_ai_works_device_request`)**  
  - Manages user requests for AI devices, including approvals and processing.  
  - Tracks fields such as **Requestor, Device Type, Justification, Approval Status, Assigned Date, etc.**  

---

### **2️⃣ Forms & UI Enhancements**  
To ensure a user-friendly experience, custom forms and UI enhancements were implemented.

#### **📝 Forms**  
- **AI Devices [Default View]** – Displays device details for easy management.  
- **Device Request [Default View]** – Allows users to submit AI device requests.  

#### **🎨 UI Formatters**  
- **Process Flow**  
  - Visual representation of the **device request lifecycle**, making it easier for users to track status.  

---

### **3️⃣ Server-Side Development**  
To automate backend processes, **Scheduled Script Executions and Events** were implemented.

#### **⏳ Scheduled Script Executions**  
- **Reminder Pickup**  
  - Automatically triggers reminders for pending **device pickups** to avoid delays.  

#### **📌 Event Registry**  
- **x_1425035_ai_works.pickup**  
  - Custom event that fires when a **device pickup request is approved** to initiate further actions.  

---

### **4️⃣ Client-Side Development**  
To enhance the front-end behavior, multiple **Client Scripts and UI Policies** were developed.

#### **💻 Client Scripts**  
- **Hide the Sections**  
  - Dynamically hides unnecessary form sections based on the selected **device category**.  
- **Show the Sections**  
  - Unhides sections when certain conditions are met (e.g., approval status changes).  

#### **⚙️ UI Policies**  
- **Additional Comments Field – Visibility & Mandatory**  
  - Ensures users provide a justification when requesting devices.  
- **Hide/Mandatory Delivery Date Field**  
  - Enforces **delivery date selection** based on request priority.  
- **Mandatory Business Justification Field**  
  - Enforces a mandatory field for **business justification** before submission.  

---

### **5️⃣ Access Control & Security**  
Role-based access controls (RBAC) and ACLs ensure that only authorized users can access specific data.

#### **👥 Custom Roles**  
- **AI Devices User (`x_1425035_ai_works_ai_devices_user`)**  
  - Can view and manage assigned AI devices.  
- **Device Management (`x_1425035_ai_works.device_management`)**  
  - Handles AI device allocation and deallocation.  
- **Dispatch Management (`x_1425035_ai_works.dispatch_management`)**  
  - Manages logistics and ensures proper delivery of AI devices.  
- **End User (`x_1425035_ai_works.end_user`)**  
  - Can submit requests and track status updates.  
- **Release Management (`x_1425035_ai_works.release_management`)**  
  - Oversees the AI device lifecycle and upgrades.  

#### **🔒 Access Control (ACLs) Implemented**  
- **CRUD Permissions** on AI Devices and Device Requests.  
- **Ownership-Based Restrictions**  
  - Users can modify only the records **they created**.  
  - Admins have full access across all records.  

---

### **6️⃣ Application Navigation & UI Modules**  
To ensure a **structured and easy-to-use interface**, custom menus and modules were designed.

#### **📌 Application Menus**  
- **AI Worksite Manager**  
  - Serves as the main navigation hub for AI device management.  

#### **📂 Modules**  
- **Active Device Request** – View ongoing AI device requests.  
- **All Device Requests** – Access a complete list of submitted requests.  
- **Closed Requests** – Archive of completed or rejected requests.  
- **Create New Device Request** – Interface to submit new AI device requests.  
- **Device Details** – Displays individual device information.  
- **Open - Unassigned Requests** – Lists pending unassigned requests.  
- **Update New Device** – Modify device information when necessary.  

#### **📱 Mobile Support**  
- **Mobile-Friendly Modules** allow access to AI device requests from mobile devices.  

---

### **7️⃣ Notifications & User Alerts**  
Automated notifications ensure that users stay informed.

#### **📩 Notifications**  
- **Reminder to the User** – Automatically triggers email/SMS reminders for pending approvals and device pickups.  

---

### **8️⃣ Service Catalog & Request Management**  
To streamline AI device ordering, **Service Catalog Items** were introduced.

#### **🛒 Service Catalog Items**  
- **Order AI Devices** – Allows users to request AI devices through a structured form.  

#### **📜 Catalog Client Scripts**  
- **Amount Calculation** – Dynamically calculates the cost of ordered devices.  
- **Field Validation** – Ensures users provide accurate input for request submission.  

---

### **9️⃣ Inbound Integrations & Data Transformation**  
To ensure smooth data import and synchronization, **Transform Maps** were configured.

#### **🔄 Table Transform Maps**  
- **Device Transform** – Automates the mapping and transformation of imported AI device data.  

---

### **🔟 Business Workflows & Flow Designer Automation**  
Using **ServiceNow Flow Designer**, an automated workflow for device requests was implemented.

#### **⚡ Flows**  
- **Order AI Device Flow**  
  - Automates the entire lifecycle of a device request:  
    1. **Request Submission**  
    2. **Manager Approval**  
    3. **Device Assignment**  
    4. **Notification to User**  
    5. **Device Pickup Confirmation**  

---

## **🛠️ Technologies & ServiceNow Features Used**  
- **ServiceNow Studio** – Custom application development.  
- **Client & Server Scripts** – Enhancing application logic.  
- **UI Policies & Formatters** – Improving UI/UX.  
- **Scheduled Script Executions & Events** – Automating backend processes.  
- **Flow Designer** – Workflow automation.  
- **Access Control Lists (ACLs) & Role-Based Security** – Restricting data access.  
- **Service Catalog & Request Management** – Managing AI device requests.  
- **Notifications** – Keeping users informed.  
- **Transform Maps** – Handling inbound data integrations.  

---

## **🚀 Conclusion**  
**AI Worksite Management** is a robust, end-to-end ServiceNow application that streamlines AI device tracking, request management, and operational workflows. It **leverages automation, security, and UI enhancements** to improve efficiency in managing AI-powered devices across worksites.  
