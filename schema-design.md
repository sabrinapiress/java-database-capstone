## MySQL Database Design

### Table: patients
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `name` VARCHAR(100) NOT NULL  
- `birth_date` DATE NOT NULL  
- `email` VARCHAR(100) UNIQUE NOT NULL  
- `phone` VARCHAR(15)  

### Table: doctors
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `name` VARCHAR(100) NOT NULL  
- `specialty` VARCHAR(100)  
- `email` VARCHAR(100) UNIQUE NOT NULL  

### Table: appointments
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `patient_id` INT NOT NULL FOREIGN KEY REFERENCES patients(id)  
- `doctor_id` INT NOT NULL FOREIGN KEY REFERENCES doctors(id)  
- `appointment_date` DATETIME NOT NULL  
- `status` VARCHAR(50) DEFAULT 'scheduled'  

### Table: administrators
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `username` VARCHAR(50) UNIQUE NOT NULL  
- `password_hash` VARCHAR(255) NOT NULL  
- `role` VARCHAR(50) NOT NULL  

---

## 📄 MongoDB Collection Design

### Collection: prescriptions

```json
{
  "prescription_id": "RX123456",
  "patient_id": 101,
  "doctor_id": 202,
  "issue_date": "2025-08-01T10:30:00Z",
  "medications": [
    {
      "name": "Amoxicillin",
      "dosage": "500mg",
      "frequency": "3 times a day",
      "duration": "7 days"
    },
    {
      "name": "Ibuprofen",
      "dosage": "200mg",
      "frequency": "as needed",
      "duration": "5 days"
    }
  ],
  "notes": "The patient should avoid alcohol during treatment."
}
