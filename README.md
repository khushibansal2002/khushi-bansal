# khushi-bansal

This is a web-based project developed using Java, JDBC, Servlets, and MySQL on the backend, while HTML, CSS, and Bootstrap are used for the frontend. The project serves as a medical website designed for hospitals, allowing patients to schedule appointments, review doctors, and view all available hospital services. The website also includes contact details of the hospital and showcases key features offered by the hospital. Separate login pages are provided for admin, doctors, and users.



##USE CASE


User [Actor]
  - Register
  - Login
  - Contact
  - Make Appointment
  - See Services
  - Review

Healthcare Provider [Actor]
  - Login
  - Contact
  - See Appointments
  - See Patient Reviews

User --> Register
User --> Login
User --> Contact
User --> Make Appointment
User --> See Services
User --> Review

Healthcare Provider --> Login
Healthcare Provider --> Contact
Healthcare Provider --> See Appointments
Healthcare Provider --> See Patient Reviews



##ER DIAGRAM 

ENTITY: Patient
Attributes:
- Patient_ID (Primary Key)
- Name
- Contact_Information
- Password

ENTITY: Medical Service
Attributes:
- Service_ID (Primary Key)
- Service_Name
- Service_Description
- Service_Availability

ENTITY: Appointment
Attributes:
- Appointment_ID (Primary Key)
- Patient_ID (Foreign Key)
- Service_ID (Foreign Key)
- Appointment_Date_and_Time
- Notes_Concerns

ENTITY: Healthcare Provider
Attributes:
- Provider_ID (Primary Key)
- Provider_Name
- Contact_Information

ENTITY: Patient Review
Attributes:
 
- Review_Text
- Rating

RELATIONSHIPS:
- Patient (1) ----- (N) Appointment
- Medical Service (1) ----- (N) Appointment
- Patient (1) ----- (N) Patient Review
- Healthcare Provider (1) ----- (N) Patient Review
