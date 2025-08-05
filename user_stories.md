# User Story
---

## User Stories - Administrators

**Title:** Administrator - Login to the portal  
_As an administrator, I want to log in to the portal with username and password, and then manage the platform securely_  
**Acceptance Criteria:**  
1. The administrator can enter valid username and password.  
2. The system validates the credentials and grants access.  
3. The administrator is redirected to the main dashboard after successful login.  
**Priority:** High  
**Story Points:** 3  
**Notes:**  
- There should be error handling for invalid login.  
---

**Title:** Administrator - Logout from the portal  
_As an administrator, I want to log out from the portal, and then protect system access_  
**Acceptance Criteria:**  
1. The administrator can click 'Logout' in the menu.  
2. The system ends the current session.  
3. The administrator is redirected to the login screen.  
**Priority:** High  
**Story Points:** 2  
**Notes:**  
- Sessions should expire automatically after inactivity.  
---

**Title:** Administrator - Add doctors  
_As an administrator, I want to add doctors to the portal, and then allow them to use the system_  
**Acceptance Criteria:**  
1. The administrator can fill in doctor data.  
2. The system validates and saves the data.  
3. The new doctor appears in the user list.  
**Priority:** High  
**Story Points:** 4  
**Notes:**  
- There should be email duplication validation.  
---

**Title:** Administrator - Delete doctor profile  
_As an administrator, I want to delete a doctor's profile from the portal, and then remove access for inactive doctors_  
**Acceptance Criteria:**  
1. The administrator can select a doctor and click 'Delete'.  
2. The system asks for confirmation.  
3. The profile is removed from the database.  
**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- Deleted profiles should be archived before removal.  
---

**Title:** Administrator - Execute MySQL procedure  
_As an administrator, I want to execute a stored procedure in the MySQL CLI, and then obtain the number of appointments per month and track statistics_  
**Acceptance Criteria:**  
1. The administrator accesses the MySQL CLI.  
2. Executes the stored procedure successfully.  
3. Receives monthly appointment statistics.  
**Priority:** High  
**Story Points:** 5  
**Notes:**  
- Procedure must be documented and secure.  
---

## User Stories - Patient

**Title:** Patient - View list of doctors without login  
_As a patient, I want to see a list of available doctors without logging in, so that I can explore options before registering._  
**Acceptance Criteria:**  
1. The system displays a list of available doctors without requiring login.  
2. The list includes specialty, name, and availability.  
3. The patient can click to see more doctor details.  
**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- The list should update automatically based on availability.  
---

**Title:** Patient - Register with email and password  
_As a patient, I want to register using my email and password so I can book appointments._  
**Acceptance Criteria:**  
1. The patient can fill out a registration form with email and password.  
2. The system validates the data and creates an account.  
3. The patient receives registration confirmation.  
**Priority:** High  
**Story Points:** 5  
**Notes:**  
- There should be email duplication validation.  
---

**Title:** Patient - Login to the portal to manage bookings  
_As a patient, I want to log in to the portal so I can manage my bookings._  
**Acceptance Criteria:**  
1. The patient can access the portal with email and password.  
2. The system displays scheduled appointments.  
3. The patient can cancel or reschedule appointments.  
**Priority:** High  
**Story Points:** 5  
**Notes:**  
- Session should expire after inactivity.  
---

**Title:** Patient - Logout from the portal  
_As a patient, I want to log out from the portal to protect my account._  
**Acceptance Criteria:**  
1. The patient can click “Logout” to end the session.  
2. The system redirects to the home page.  
3. The session ends securely.  
**Priority:** Medium  
**Story Points:** 2  
**Notes:**  
- There should be visual confirmation of logout.  
---

**Title:** Patient - Book a one-hour appointment  
_As a patient, I want to book a one-hour appointment with a doctor so I can receive medical care._  
**Acceptance Criteria:**  
1. The patient can select doctor, date, and time.  
2. The system checks availability and confirms booking.  
3. The patient receives appointment notification.  
**Priority:** High  
**Story Points:** 5  
**Notes:**  
- There should be a limit of one appointment per doctor per time slot.  
---

## User Stories - Doctor

**Title:** Doctor - Set availability  
_As a doctor, I want to set my available hours so that patients can book appointments accordingly._  
**Acceptance Criteria:**  
1. The doctor can add available hours.  
2. The doctor can edit or remove hours.  
3. Patients can only book within the defined hours.  
**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- There should be conflict checking with already scheduled appointments.  
---

**Title:** Doctor - Login to the portal  
_As a doctor, I want to log in to the portal so I can manage my appointments._  
**Acceptance Criteria:**  
1. The doctor can access the portal with valid email and password.  
2. The system validates credentials and redirects to the doctor dashboard.  
3. Error messages are displayed in case of login failure.  
**Priority:** High  
**Story Points:** 3  
**Notes:**  
- Login should be protected by secure authentication.  
---

**Title:** Doctor - Logout from the portal  
_As a doctor, I want to log out from the portal to protect my data._  
**Acceptance Criteria:**  
1. The doctor can click 'Logout' to end the session.  
2. The session ends and the user is redirected to the home page.  
3. No sensitive data remains accessible after logout.  
**Priority:** High  
**Story Points:** 2  
**Notes:**  
- Logout should work across all browsers.  
---

**Title:** Doctor - Display appointment calendar  
_As a doctor, I want to see my appointment calendar so I can stay organized._  
**Acceptance Criteria:**  
1. The doctor can view future and past appointments.  
2. Appointments are shown with date, time, and patient name.  
3. The calendar allows navigation by month and week.  
**Priority:** High  
**Story Points:** 4  
**Notes:**  
- The calendar should be responsive and easy to use.  
---

**Title:** Doctor - Mark unavailability  
_As a doctor, I want to mark unavailable times so that only available slots are shown to patients._  
**Acceptance Criteria:**  
1. The doctor can select dates and times as unavailable.  
2. These times are not shown for patient booking.  
3. The system prevents booking in blocked times.  
**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- There should be visual confirmation of blocked times.  
---

**Title:** Doctor - Update profile  
_As a doctor, I want to update my specialty and contact information so that patients have up-to-date information._  
**Acceptance Criteria:**  
1. The doctor can edit specialty, phone, and email.  
2. Changes are saved and reflected in the public profile.  
3. The system validates fields before saving.  
**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- The profile should be updated in real-time.  
---

**Title:** Doctor - View patient details  
_As a doctor, I want to view patient details for upcoming appointments so I can be prepared for the consultation._  
**Acceptance Criteria:**  
1. The doctor can access information of scheduled patients.  
2. Data includes medical history and previous prescriptions.  
3. Access is restricted to patients with scheduled appointments.  
**Priority:** High  
**Story Points:** 4  
**Notes:**  
- There should be secure access control to the data.  
