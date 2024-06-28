# Appointment System Database Schema

This database schema is designed to manage appointments between users, doctors, and clinics.

### Tables

1. *users*
   - id INT: Primary key for the user.
   - name VARCHAR(255): Name of the user.
   - birthdate DATE: Birthdate of the user.

2. *doctors*
   - id INT: Primary key for the doctor.
   - name VARCHAR(255): Name of the doctor.

3. *clinics*
   - id INT: Primary key for the clinic.
   - name VARCHAR(255): Name of the clinic.

4. *appointments*
   - id INT: Primary key for the appointment.
   - user_id INT: Foreign key referencing users(id).
   - doctor_id INT: Foreign key referencing doctors(id).
   - clinic_id INT: Foreign key referencing clinics(id).
   - appointment_time DATETIME: Date and time of the appointment.
   - status ENUM('booked', 'cancelled'): Status of the appointment.
   - created_at TIMESTAMP: Timestamp for when the appointment was created.
