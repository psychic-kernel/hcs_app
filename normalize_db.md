# hcs app - Database normalization

1. User Entities

# Patients 

ID, 
name, 
DOB, 
gender, 
email, 
phone, 
address, 
profile picture, 
medical history, 
allergies, 
insurance details, 
preferred doctor

# Doctors 

(ID, 
name, 
specialization, 
qualifications, 
email, 
phone, 
address, 
profile picture, 
availability, 
license number, 
consultation fee, 
hospital affiliation, 
ratings/reviews)

# Admins 

(ID, 
name, 
email, 
role, 
permissions, 
activity logs)

# Pharmacists 

(ID, 
name, 
email, 
pharmacy name, 
license number, 
contact details)


2. Authentication & Security

# User Credentials 
(user ID, 
password hash, 
jw tokens, 
last login)

# Session Logs 
(session ID, 
user ID, 
IP address, 
login time, 
logout time, 
device info)

# Access Control 
(user ID, 
role, 
permissions, 
status)

# Audit Logs 
(log ID, 
user ID, 
action type, 
timestamp, 
affected entity)


3. Appointments & Scheduling

# Appointments 
(appointment ID, 
patient ID, 
doctor ID, 
date/time, 
status, 
consultation type [virtual/in-person], 
reason for visit, 
notes, 
prescription ID)

# Doctor Availability 
(doctor ID, 
available days/times, 
holidays, 
max appointments per day)

# Reminders 
(reminder ID, 
user ID, 
appointment ID, 
type [email/SMS/push], 
sent status, 
timestamp)


4. Communication & Interaction

# Messages 
(message ID, 
sender ID, 
receiver ID, 
content, 
timestamp, 
read status)

# Video Calls 
(call ID, 
patient ID, 
doctor ID, 
start time, 
end time, 
duration, 
recording link)

# Chatbot Interactions 
(interaction ID, user ID, query, AI response, timestamp)


5. Medical Records & Prescriptions

# Medical Reports (report ID, patient ID, doctor ID, file URL, upload date, description)

# Prescriptions (prescription ID, patient ID, doctor ID, medication list, dosage, duration, notes, issued date)

# Test Results (test ID, patient ID, doctor ID, lab name, test type, result, report file URL, test date)

# Allergies & Conditions (record ID, patient ID, condition name, severity, notes, diagnosis date)


6. Billing & Payments

# Invoices 

(invoice ID, patient ID, doctor ID, appointment ID, total amount, status [paid/pending], payment method, issue date)

# Transactions 

(transaction ID, invoice ID, user ID, payment gateway, amount, timestamp, status)

# Subscription Plans 

(plan ID, user ID, type [free/premium], start date, expiry date, auto-renewal status)


7. Notifications & Alerts

Push Notifications (notification ID, user ID, type [reminder/alert], content, timestamp, read status)

Email Logs (log ID, user ID, email type, sent status, timestamp)


8. Health Monitoring & Wearable Data

Vitals Readings (record ID, patient ID, date/time, heart rate, blood pressure, glucose level, oxygen saturation)

Device Integration Logs (log ID, patient ID, device name, sync status, last sync time)




