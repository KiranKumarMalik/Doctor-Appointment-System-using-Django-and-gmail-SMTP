<h1 align="center"> <img src="https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/ed8bc15f1f6c1988592ead3c361e6ca402f5ab8d/static/appoint_app/images/appointment_doctor.png" alt="appoint-master-dark" width="55" height="55" style="vertical-align: middle;"><span style="font-size: 28px;">Doctor Appointment System </span> </h1>

## *Doctor Appointment Management System using Django*

[Appoint Master](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP)**©** 2025, All Rights Reserved 


# System Documentation  

### OVERVIEW

➢ **Electronic Appoint Master** is a Doctor-Patient Appointments Management System. This system was originally meant for Kenyatta University Health Centre (Organization) - [KUHC](https://www.ku.ac.ke/healthunit/).  

➢ Appoint Master steps in to make things easier for KUHC patients to book an appointment with their doctors. It tries to automate the process of booking doctor appointments from the old-school manual system.

> [!NOTE] 
> Appoint Master **only** acts as an **intermediary** between the *patients* and *KUHC*; and thus ***does not go into the details of what happens during the appointments*** (any medical procedures). 

### Users

The system is restricted to:  
➢ **Students**,  
➢ **Staff**, and  
➢ **Doctors** of Kenyatta University - [KU](https://www.ku.ac.ke/). 

> [!NOTE]   
>  Any Validation rules used in the system are in compliance with the KU system, such as user IDs. The **Admin** is also a user of the system; probably a member of the staff (but not a staff patient!).  

### Features

#### 1. Account Creation

➢ ***Patients*** (Students & Staff) can create their own Appoint Master account (by filling a registration form), and then get started right away. As for the ***Doctors*** and ***other Admins***, the admin (main) is responsible for creating a customized account for each one of them. 

> [!IMPORTANT]  
> All Users can also **delete** their accounts (permanently) if they choose to.

#### 2. Appointments Management

➢ Patients can ***book*** a doctor appointment, ***cancel*** it and even ***delete*** the appointments. Patients can also ***view*** all their appointments, that is, **Scheduled, Failed, Canceled**, and **Completed**. Doctors can ***view all appointments*** meant for them, for instance, dentists will only see appointments from patients with dental problems. Doctors can also ***close*** an appointment once it's completed. Admins can ***view*** and ***manage all appointments***; they can ***create, cancel, close*** and ***delete*** an appointment.  

> [!NOTE]   
> When looking at details about a specific appointment, the Patient and the Doctor have different page views. For instance, the patient can generate a report about that particular appointment while the doctor can't. The patient can also view their personal details such as *phone number* and *email* used for that appointment; the doctor won't see the patient's *phone number* or *email* when checking details about a specific appointment.

#### 3. Electonic Payments

➢ Patients can pay for their appointments electronically via the  ***[PayStack API](https://paystack.com/docs/api/)*** by either using their ***M-Pesa*** or ***Visa***. After payment verification, it's only when the appointments can be deemed to be scheduled.  

#### 4. SMTP Mail Service

➢ Appoint Master is incorporated with the ``send_mail`` service to send relevant emails to the users, based on certain operations. For instance, when patients ***book, pay for, cancel,*** or even ***delete*** an appointment, an email is sent to them. Doctors also get an email notifying them of newly booked or canceled appointments (by patients, meant for them).  

#### 5. One Time Password(OTP) Verification

➢ OTP (One-Time Password) verification is a security mechanism used to authenticate users and verify their identity. In Appoint Master, this is achieved by the system sending 6-digit codes to **Doctors** and **Admins** via email during login. It's an added layer of security on top of the normal login page, to further validate high-level users.  

> [!NOTE]   
>  This feature is not fully implemented (is incomplete). May require addition of time-sensitivity; OTPs to expire after a specific period of time. 

#### 6. User Logging

➢ Every user's login session is captured by the system. For instance, the admin can trace which user logged into their accounts at what particular time, thus making it easier to account for any issues with the system, by tracing when and where (which user) the problems originated from.

#### 7. Account Deactivation/Activation

➢ The Admin can deactivate user accounts, upon which the respective users would be locked out of their accounts. The Admin can also activate the accounts back, upon which the relevant users can now have access to their accounts (unlocked).

#### 8. Next-of-Kin

➢ Patients can add information regarding their next-of-kin, and the next-of-kin are linked to those particular patients. Therefore, if for instance the patient account (with next-of-kin) is deleted, their next-of-Kins are also deleted along with it.   

> [!NOTE]   
>  This feature is not fully implemented (is incomplete). May require addition of next-of-kin actions in the system such as appointment booking. 

#### 9. Reports Generation

➢ The system can be used to generate reports for patient appointments and payments. Admins can generate reports of all payments and appointments for all the patients. Patients can generate a report of a specific appointment, and all their payments too.

> [!NOTE]   
>  This feature is not fully implemented (is incomplete). May need to be customized based on various dates and time.

#### 10. Data Analytics

➢ The system can show real data analytics (statistically) of appointments [Booked, Scheduled, Failed, Canceled, Completed, Closed], Payments [Mpesa transactions] and Active/Registered Patients [Student Cover, MediCare Cover-Staff]. See the screenshot below (Admin, Patient, & Doctor Dashboard).  

![analytics-admin](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/1ce58c1d0402fe83335d68883a4aa1897795400e/ss/admin.png)
![patient-dashboard-analytics](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/1ce58c1d0402fe83335d68883a4aa1897795400e/ss/patient.png)
![doctor-dashboard-analytics](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/1ce58c1d0402fe83335d68883a4aa1897795400e/ss/doctor.png)

#### 11. Flexible Patient ID registration

➢ It is possible to create new patient IDs (by Admin), which are initially set to unregistered. These IDs are linked to the registration system, where by registration is only possible for IDs already in the system. Once the patient fills the registration form successfully, the ID (which was initially unregistered) becomes registered under that user. Any attempt to create an account with same ID is revoked by the system.   

> [!IMPORTANT]   
> If an account of a registered user is deleted, the user ID remains in the database, but the ID's status now changes from registered to unregistered; a new user can now register with that ID (again). 

## SCREENSHOTS

### Homepage

![home1](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/e8d3393b435a591c8003293ee373da61fe160fdb/ss/Screenshot%202025-04-10%20214445.png)![home2](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/e8d3393b435a591c8003293ee373da61fe160fdb/ss/Screenshot%202025-04-10%20214505.png)![home3](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/e8d3393b435a591c8003293ee373da61fe160fdb/ss/Screenshot%202025-04-10%20214523.png)![home4](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/e8d3393b435a591c8003293ee373da61fe160fdb/ss/Screenshot%202025-04-10%20214545.png)

### Account Login

![User-login](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/e8d3393b435a591c8003293ee373da61fe160fdb/ss/Screenshot%202025-04-10%20214722.png)

### 1. Patients

#### Registration

![Patient-registration](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/48039daaac7050c14f6823f4985efdcbd916ed87/ss/Screenshot%202025-04-10%2021593.png)

#### Patient Login (Student)

![Student-patient-login](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/48039daaac7050c14f6823f4985efdcbd916ed87/ss/Screenshot%202025-04-10%20220655.png)

#### Reset Password

##### Forgotten Password-Email

![Reset-email](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/96aff9a728a082017d62149b3f16606bc6036341/ss/Screenshot%202025-04-11%20112843.png)

> [!IMPORTANT]  
> You have to enter an existing email; already registered in the database, otherwise it won't work.

##### Reset success!

![reset-done](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/96aff9a728a082017d62149b3f16606bc6036341/ss/Screenshot%202025-04-11%20112857.png)

##### Reset link (Email)

![reset-email-link](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/96aff9a728a082017d62149b3f16606bc6036341/ss/Screenshot%202025-04-11%20112928.png)

##### Password Reset Page

![password-reset-page](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/96aff9a728a082017d62149b3f16606bc6036341/ss/Screenshot%202025-04-11%20113000.png)

##### Reset Complete

![reset-complete](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/96aff9a728a082017d62149b3f16606bc6036341/ss/Screenshot%202025-04-11%20113016.png)

##### Expired Reset Link

![expired-link](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/0447c616879fad55db0bf76a17a1da33db9a8d6b/ss/Screenshot%202025-04-11%20113814.png)

#### Student Profile Update

![student-profile](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/b078ea8fedd693b57b2e13e8ba4141be6cc27f91/ss/Screenshot%202025-04-11%20114227.png)

#### Student (Next-of-kin) Profile Update

![next-of-kin](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/291b069d3c2c7a165dd169d43e1f5a9ae749ca65/ss/Screenshot%202025-04-11%20193025.png)

#### Appointment Booking

##### Registration Page

![appoint-registration](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20221718.png)

##### Initiate Payment

![initiate-payment](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20221736.png)

##### Initiate Payment>Confirmed

![initiate-payment-confirmed](https://i.imgur.com/sqsYhFc.png)

##### Initiate Payment>Accepted

![initiate-payment-accepted](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20221752.png)

##### Checkout Page

![checkout-page](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20221820.png)

##### Payment successful!

![payment-success](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20221848.png)

#### Payments

##### View all your Payments

![student-view-payments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5edea235a466d2dc9ede0f2656d29bbe33c1308a/ss/Screenshot%202025-04-10%20222950.png)

##### Payments Report

![student-payments-report](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/43c45ed7cb4f400bf6f4bf93ca6b155d34012680/ss/Screenshot%202025-04-11%20195849.png)

#### Appointments

##### View all Appointments

![view-all-student-appointments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/f3f083fb1ced66cb48cea55f5d3014ed34d65f6e/ss/Screenshot%202025-04-10%20222853.png)

##### Manage all Appointments

![manage-appointments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/f3f083fb1ced66cb48cea55f5d3014ed34d65f6e/ss/Screenshot%202025-04-10%20222917.png)

##### View Appointment Details> by Appoint ID

![appoint-id-details](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c47d28960cd8ff65f315422e62a757258fa8d76a/ss/Screenshot%202025-04-11%20200446.png)

##### Appointment Report (by Appoint ID)

![appointment-report-by-id](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/b30c11ddf49d4f2488729b41f92b8e1315414376/ss/Screenshot%202025-04-11%20201004.png)

#### Delete User Account Permanently!

![Delete-user-account-permanently](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/eeaa8c96ef0c1930422ad4d71d94c3029ae1adf0/ss/Screenshot%202025-04-12%20085523.png)

### 2. Admin

#### Account Login

##### Login Page

![admin-login-page](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/b30c11ddf49d4f2488729b41f92b8e1315414376/ss/Screenshot%202025-04-10%20214722.png)

##### OTP Verification (if Login is successful)

![admin-otp-verification](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/b30c11ddf49d4f2488729b41f92b8e1315414376/ss/Screenshot%202025-04-10%20214748.png)
![otp-email](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/9b5ed98fbc0a60677b2cb6b48484856b586e9468/ss/Screenshot%202025-04-11%20201946.png)
![otp-ver-failed](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/9b5ed98fbc0a60677b2cb6b48484856b586e9468/ss/admin.png)

> [!TIP]
> You can directly log in as Admin (*Jazzmin Dashboard*) without the whole OTP verification by using the link "http://127.0.0.1:8000/admin/". You'll get the a different login page(as below) where you'll be prompted to enter your *Username* and *Password*; and that's it! You're logged in. Once logged in, you can navigate to the *Main Dashboard* (See other screenshots below).

![jazzmin-login](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/fe9c98cd766decf4d59e46c80f224e6ccd8bcff8/ss/Screenshot%202025-04-11%20202529.png)

#### Admin Dashboard(s)

##### (a) Main Dashboard

![admin-dash-dark](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/9b5ed98fbc0a60677b2cb6b48484856b586e9468/ss/admin.png)

##### (b) Jazzmin Dashboard

![jazzmin-dashboard](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/fe9c98cd766decf4d59e46c80f224e6ccd8bcff8/ss/Screenshot%202025-04-11%20202547.png)

> [!IMPORTANT]
> To access the Jazzmin dashboard, click the "**Dashboard**" button (top-left of the *Main Dashboard*). To go back to the *Main Dashboard*, click the "**Back to Site**" link (top-left-near-center of the *Jazzmin Dashboard*).

#### Admin Profile Update

![update-profile](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/7248391f655951c2a74978e38e66ed7c2a851c88/ss/Screenshot%202025-04-11%20203312.png)

#### View All Appointments

![admin-view-all-appointments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/7248391f655951c2a74978e38e66ed7c2a851c88/ss/Screenshot%202025-04-10%20223357.png)

##### All Appointments Report

![all-appointments-report-pdf](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c1fc8981a878af140eb09c9304ea701eee6e05f7/ss/Screenshot%202025-04-11%20204138.png)

#### Manage all Appointments

![manage-all-appointments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/7248391f655951c2a74978e38e66ed7c2a851c88/ss/Screenshot%202025-04-10%20223357.png)
![manage-all-appoints-jazzmin](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/8541cb6dd4195f3bc2bff120157b3362e2c9a636/ss/Screenshot%202025-04-10%20223513.png)

#### View all Payments

![admin-all-payments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/8541cb6dd4195f3bc2bff120157b3362e2c9a636/ss/Screenshot%202025-04-10%20223416.png)

#### View all Payments Report

![all-payments-report](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/8541cb6dd4195f3bc2bff120157b3362e2c9a636/ss/Screenshot%202025-04-11%20194813.png)

#### Manage all Payments

![all-payments-manage](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/8541cb6dd4195f3bc2bff120157b3362e2c9a636/ss/Screenshot%202025-04-10%20223527.png)

#### Manage all Users

![manage-all-users](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/8541cb6dd4195f3bc2bff120157b3362e2c9a636/ss/Screenshot%202025-04-10%20223540.png)
![deactivate-users](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/a7ce827ce8cfddcb320741be692951897b8584e2/ss/Screenshot%202025-04-11%20205405.png)

#### Doctor Registration

![doctor-reg](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c30ca374a1e72c82131a77f815341bdcc770df46/ss/Screenshot%202025-04-10%20215156a.png)

#### Admin registration

![admin-registration](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c66a32bbd17ac3d9854b12067e43c0a3ce26de11/ss/Screenshot%202025-04-11%20210852.png)

#### OTP Login History

![otp-login-history](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c30ca374a1e72c82131a77f815341bdcc770df46/ss/Screenshot%202025-04-10%20223653.png)

#### Patient IDs

![patient-ids-add](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c30ca374a1e72c82131a77f815341bdcc770df46/ss/Screenshot%202025-04-10%20223614.png)
![patient-ids-staff](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/c30ca374a1e72c82131a77f815341bdcc770df46/ss/Screenshot%202025-04-10%20223626.png)

### 3. Doctors

#### Doctor Login details (Email from Admin)

![doctor-registered-email](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/735aecedb4b0a9a139e547722acf8af1997240ce/ss/Screenshot%202025-04-11%20212321.png)

#### Login

![doctor-login](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/735aecedb4b0a9a139e547722acf8af1997240ce/ss/Screenshot%202025-04-10%20221957.png)

##### OTP Verification

![otp-verify-doctor](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/735aecedb4b0a9a139e547722acf8af1997240ce/ss/Screenshot%202025-04-10%20222021.png)
![otp-verification-email](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/5264705d8ca2806a56c0080e1074d52e164dfcd7/ss/Screenshot%202025-04-11%20212650.png)

### Doctor Dashboard

##### Dark Mode

![doctor-dashboard-dark1](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/29a8a2238abc0e08fe4acd607de7f133bb09e91b/ss/doctor.png)

##### New Appointment

![doctor-email-new-appointment](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/1b875179397a8585878dd84762ba7e04fcd21346/ss/Screenshot%202025-04-12%20083259.png)


##### Closed Appointment

![closed-appointment-doctor](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/d7b960c9cff144c12490890c6615744540d925b3/ss/Screenshot%202025-04-12%20083552.png)

### Doctor Profile Update

![doctor-profile-update](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-12%20084222.png)

### Scheduled Appointments

![doctor-scheduled-appointment](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-10%20222251.png)

### Manage Appointments

![doctor-manage-appointment](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-10%20222328.png)
![doctor-action](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-10%20222341.png)
![doctor-appointment-close](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-10%20222407.png)  

### View Closed Appointments

![view-closed-appointments](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-10%20222458.png)

### Appointment Payment Receipt in Mail

![doctor-receipt-mail](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/77b00787a49c023b9a73cf9f04e238b4eea3775e/ss/Screenshot%202025-04-12%20083619.png)

## INSTALLATION

### Prerequisites

> [!IMPORTANT]
> Ensure that you've installed the dependencies below, before continuing to the next part. If you already installed them, you may skip this part.  

```
Python 3.12.3 (+)
Pip
Node.js and npm (for managing Tailwind CSS)
Visual Studio(VS) Code
```

> [!NOTE]
> This project is implemented on a Windows 11 Operating System (OS).

#### Useful links

1. Download **Python** (Latest version): https://www.python.org/downloads/  
2. Download the Pip file: https://bootstrap.pypa.io/get-pip.py  
   ➢ More details about pip: https://pip.pypa.io/en/stable/installation/

![Pip installation](https://i.imgur.com/iG4RV83.png)

3. Node.js installer: https://nodejs.org/en/download/prebuilt-installer  
4. VS Code: https://code.visualstudio.com/download
5. Tailwind CSS installation Guide: [Worth understanding how to install!](https://django-tailwind.readthedocs.io/en/2.3.0/installation.html)

> [!TIP]
> You need to add the installed tools (*Python, Node.js & npm, VS Code*) to PATH. Check out guide [here](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/).

### Getting Started

➢ Download the Project by either:

1. Using the direct GitHub download link: https://github.com/Lewismwaz/appoint_master/archive/refs/heads/main.zip 
   or 
2. Typing the command below on the terminal. ([Git](https://www.git-scm.com/downloads) must be installed in your system!)  

```
   git clone https://github.com/Lewismwaz/appoint_master.git  
```


➢ Download the project's **node_modules** from [here.](https://drive.google.com/drive/folders/1omUN1Lm2mAPxZYOaFq3BuFg_DPHYL_xE) Extract the zip file, then copy and paste it into appoint_master (project folder) as shown below.  
![node_modules](https://i.imgur.com/jOuhAw1.png)
##### SMTP Server setup>Email

➢ Open the downloaded project folder(appoint_master). Right-click and select the option ***Open with VS Code***.   Click on the explorer (on the left) then navigate to: ***appoint→settings.py***

➢ Set up your default email for Django: [Django SMTP Server setup Guide](https://medium.com/django-unleashed/configuring-smtp-server-in-django-a-comprehensive-guide-91810a2bca3f)  

> [!IMPORTANT]
> You need to replace your email credentials in the *settings.py* file, as shown below. Find the email configuration in (***line 12-20***)

![Django Email Settings](https://i.imgur.com/caGebc0.png)

Check out the implementation below, using 'gmail' email-provider: 

> [!CAUTION]
> The email credentials **EMAIL_HOST_USER**, and **EMAIL_HOST_PASSWORD** below are not real! You need to replace them with your actual credentials. They're only just for demonstration.

```python
# settings.py

# SMTP Email Backend setup
EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'

EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_HOST_USER = 'janedoe@gmail.com'
EMAIL_HOST_PASSWORD = 'aksn wygf viyp gloh'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
```

##### PayStack API setup>Payment

➢ Set up your *private* and *public* **PayStack API Keys**:  

> [!WARNING]
> The PayStack payment API used in this project is tailored for people in Kenya (M-Pesa users) only. It won't work for other countries, unless of course by modifying the payment code (Located: .\appoint_master\payments).

> [!IMPORTANT]
> You have to **create** a verified PayStack account in order to get access to the live keys (private and public), in order for payment to work. Create a PayStack account [here](https://paystack.com/ke/?q=/).  When done, log into your account. Navigate to *Settings/ApI Keys & Webhooks/*, then **copy** the *Live Secret Key* and *Live Public Key*. Ensure that live is turned on (As shown below)

![PayStack API Keys](https://i.imgur.com/99Z8jwK.png)

➢ Paste the live keys you copied, inside the *settings.py* file ***(line 156-158)***, as shown below:  

```python
# PayStack API keys
PAYSTACK_SECRET_KEY = 'sk_live_7d72f71bdeb47084024e5f7d0ba1kbbc15fd6895'
PAYSTACK_PUBLIC_KEY = 'pk_live_fdc16c020d620652ad9d948e5ceda61de4e485e7'
```

> [!CAUTION]
> These are not real keys. They're only just for demonstration! Replace them with your actual keys.

##### Virtual Environment setup>venv

➢ Inside VS Code, *open terminal*.   

> [!TIP]
> Use shortcut (**Control+Shift+~**).

➢ Install your virtual environment (venv) using the command below:  

```
python -m venv venv
```

##### Venv Activation

➢ In the terminal, activate the virtual environment using the command below:  

```psh
.\venv\Scripts\Activate.ps1
```

You should now see the (venv) before the path to the current directory (as shown below):  

![venv: Active](https://i.imgur.com/tMNcrnZ.png)

> [!IMPORTANT]
> Always ensure you activate the virtual environment (venv) before starting the server, otherwise you'll get tracebacks in the project files and also the terminal. To deactivate the venv, run the command *deactivate* on the terminal. 

##### Project Requirements

➢ Next, you need to install all the requirements below:  

```
aiohttp==3.9.3

aiohttp-retry==2.8.3

aiosignal==1.3.1

amqp==5.2.0

arabic-reshaper==3.0.0

arrow==1.3.0

asgiref==3.7.2

asn1crypto==1.5.1

attrs==23.2.0

Babel==2.14.0

beautifulsoup4==4.12.3

billiard==4.2.0

binaryornot==0.4.4

Brotli==1.1.0

cairocffi==1.7.0

celery==5.3.6

certifi==2023.11.17

cffi==1.16.0

chardet==4.0.0

charset-normalizer==3.3.2

click==8.1.7

click-didyoumean==0.3.0

click-plugins==1.1.1

click-repl==0.3.0

colorama==0.4.6

cookiecutter==2.5.0

crispy-bootstrap4==2024.1

crispy-bootstrap5==2024.2

cryptography==42.0.5

cssselect2==0.7.0

Django==5.0.1

django-browser-reload==1.12.1

django-crispy-forms==2.1

django-jazzmin==2.6.0

django-phonenumber-field==7.3.0

django-tailwind==3.8.0

django-widget-tweaks==1.5.0

djangorestframework==3.15.0

et-xmlfile==1.1.0

fonttools==4.53.0

frozenlist==1.4.1

html5lib==1.1

idna==2.10

Jinja2==3.1.3

kombu==5.3.5

lxml==5.1.0

markdown-it-py==3.0.0

MarkupSafe==2.1.4

mdurl==0.1.2

multidict==6.0.5

numpy==1.26.4

openpyxl==3.1.2

oscrypto==1.3.0

pandas==2.2.1

phonenumbers==8.13.30

pillow==10.2.0

prompt-toolkit==3.0.43

pycparser==2.21

pydyf==0.10.0

Pygments==2.17.2

pyHanko==0.23.0

pyhanko-certvalidator==0.26.3

PyJWT==2.8.0

pypdf==4.1.0

pyphen==0.15.0

pypng==0.20220715.0

python-bidi==0.4.2

python-dateutil==2.8.2

python-docx==1.1.0

python-slugify==8.0.1

pytz==2024.1

PyYAML==6.0.1

qrcode==7.4.2

reportlab==4.0.9

requests==2.31.0

rich==13.7.0

six==1.16.0

soupsieve==2.5

sqlparse==0.4.4

svglib==1.5.1

text-unidecode==1.3

tinycss==0.4

tinycss2==1.3.0

types-python-dateutil==2.8.19.20240106

typing_extensions==4.10.0

tzdata==2023.4

tzlocal==5.2

uritools==4.0.2

urllib3==1.26.18

vine==5.1.0

wcwidth==0.2.13

webencodings==0.5.1

xhtml2pdf==0.2.15

yarl==1.9.4

zopfli==0.2.3
```

➢ Use the command below to install all the requirements:  

```
pip install -r requirements.txt
```

##### Jazzmin Dashboard setup>Admin UI

Copy the *base.html* file (Located: *appoint_master→Resources*), paste and replace it inside: **venv→Lib→site-packages→jazzmin→templates→admin**. 

### Migrations

➢  For the system to function, it needs a database (db.sqlite3), which does not exist at the moment. To create one, you need to make migrations to save, synch and format for instance, the SMTP server and PayStack settings, done earlier. Run the following commands in order:  

```
python manage.py makemigrations account
python manage.py migrate account
python manage.py makemigrations payments
python manage.py migrate payments
python manage.py migrate
```

### Superuser/Admin

➢ To establish overall control over the system, an administrator is required. To create one, use the command below:  

```
python manage.py createsuperuser
```

You should get something like this (below):

![create-superuser](https://i.imgur.com/fzqIemI.png)

### Starting Server

➢ To access the system, you need to run the server. This can be achieved by **opening two separate terminals**, then typing the two commands below (one per terminal):  

> [!TIP]
> To open a new (separate) terminal, click the plus(+) icon on your terminal window's top-right(See screenshot below)

```
python manage.py runserver
python manage.py tailwind start
```

You should get something like this (below):  

![Start-Server](https://i.imgur.com/c2PiiB9.png)

> [!IMPORTANT]
> Ensure that the venv is activated before running the 2 commands; in both terminals.

> [!NOTE]
> The Timezone used for this project is "Africa/Nairobi". For users from other regions, it is recommended to replace this with your own Timezone (*Settings.py line 130*).

### Accessing the site

➢ To view the Appoint Master site, simply:

1. Press **Control+Click** in your terminal where there is "http://127.0.0.1:8000/"  
   or
2. Select, copy (*Control+C*), paste (*Control+V*) the link "http://127.0.0.1:8000/" into your browser, then press Enter.  

> [!IMPORTANT]
> Ensure you are connected to the internet when accessing the site; to load icons and also to be able to send/receive emails.

## Usage

> [!IMPORTANT]
> Before anything else, log into the admin account, and create a couple of Patient (Student & Staff) IDs. Patients can't register themselves with the system if they're not recognized already, and thus this would make things easier when it comes to validating new users wanting to register, who are not students/staff. The video demo will come in handy. See implementation [here](https://drive.google.com/file/d/1ymAbw7n1UYogrRrc1ILahWsgL54yYRdW/view?usp=drivesdk)

1. Open your browser and go to `http://127.0.0.1:8000/`.
2. Register yourself as a patient using your institution ID (Staff/Student). Reset password by selecting "forgotten password". For doctors and other admins, the admin creates their account, then the login credentials (username & password) are automatically sent to them (via email).
3. Log into Appoint Master Dashboard (if you already registered); enter username and password[Direct login for Patients only]. For Admins and Doctors, OTP Verification is required.
4. As an admin, you can manage users, patient IDs, OTP login History, payments and appointments from the admin panel. You can also generate reports for all user appointments and payments.
5. As a doctor, you can view and manage (close) your appointments.
6. As a patient, you can schedule/create, pay for, cancel, view and delete your appointments. You can also generate reports for a specific appointment and even for all your payments.

> [!CAUTION]
> All users have an option to delete their account PERMANENTLY! If they so choose to do that, then, everything about them in the system is permanently deleted.

## Technologies used

- **Backend:** Django
- **Frontend:** HTML, CSS, Tailwind CSS, JavaScript
- **Database:** SQLite (default, can be changed to PostgreSQL or other databases)
- **Version Control:** Git

## Contributing

Contributions are welcome! Please follow these steps(below) to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/your-feature`).
6. Open a pull request.

## License

This project is licensed under the MIT License. View License [here.](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP/blob/92a8f6a5f02c4ef3d2d439b907511f9d59eed7fe/LICENSE)  

More details about the MIT License can be found [here.](https://choosealicense.com/licenses/mit/)

## Contact

For any inquiries, please contact:

- Email - malikkiran413@gmail.com
- GitHub - [@Kirankumarmalik](https://github.com/KiranKumarMalik)  

[Doctor Appointment](https://github.com/KiranKumarMalik/Doctor-Appointment-System-using-Django-and-gmail-SMTP?tab=readme-ov-file)**©** 2024, All Rights Reserved
