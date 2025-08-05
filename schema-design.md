## MySQL Database Design

### Tables:

#### Table: patients
- `id`: INT, PRIMARY KEY, AUTO_INCREMENT  
- `name`: VARCHAR(100), NOT NULL  
- `email`: VARCHAR(100), UNIQUE, NOT NULL  
- `phone`: VARCHAR(15)  
- `birth_date`: DATE  
- `address`: TEXT  

#### Table: doctors
- `id`: INT, PRIMARY KEY, AUTO_INCREMENT  
- `name`: VARCHAR(100), NOT NULL  
- `specialty`: VARCHAR(100), NOT NULL  
- `email`: VARCHAR(100), UNIQUE, NOT NULL  
- `phone`: VARCHAR(15)  
- `working_hours`: TEXT (e.g., "Mon-Fri 08:00-17:00")  

#### Table: appointments
- `id`: INT, PRIMARY KEY, AUTO_INCREMENT  
- `patient_id`: INT, FOREIGN KEY → patients(id)  
- `doctor_id`: INT, FOREIGN KEY → doctors(id)  
- `appointment_time`: DATETIME, NOT NULL  
- `status`: INT (0 = Scheduled, 1 = Completed, 2 = Cancelled)  

#### Table: prescriptions
- `id`: INT, PRIMARY KEY, AUTO_INCREMENT  
- `appointment_id`: INT, FOREIGN KEY → appointments(id)  
- `description`: TEXT  
- `issued_at`: DATETIME  

#### Table: administrators
- `id`: INT, PRIMARY KEY, AUTO_INCREMENT  
- `username`: VARCHAR(50), UNIQUE, NOT NULL  
- `password_hash`: VARCHAR(255), NOT NULL  
- `role`: VARCHAR(50)  

### Constraints and Decisions

- Fields like `email`, `name`, and `appointment_time` should be validated via code.
- If a patient is deleted, appointments can be deleted via cascade or archived.
- Doctors should not have overlapping appointments — this must be handled in business logic.
- Prescriptions are tied to specific appointments to ensure traceability.


## 📄 MongoDB Collection Design

### Collection: prescriptions

```json
{
  "_id": "ObjectId('64abc123456')",
  "appointmentId": 51,
  "doctorId": 12,
  "patientId": 34,
  "medications": [
    {
      "name": "Paracetamol",
      "dosage": "500mg",
      "frequency": "1 tablet every 6 hours"
    },
    {
      "name": "Ibuprofen",
      "dosage": "200mg",
      "frequency": "Twice a day"
    }
  ],
  "doctorNotes": "Avoid alcohol during treatment.",
  "tags": ["painkiller", "anti-inflammatory"],
  "pharmacy": {
    "name": "Walgreens SF",
    "location": "Market Street"
  },
  "attachments": [
    {
      "type": "PDF",
      "url": "https://clinic.com/prescriptions/123.pdf"
    }
  ],
  "issuedAt": "2025-08-05T10:30:00Z"
}

