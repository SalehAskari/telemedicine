# Classes

```
class Patient:
patient_id
name
family
national_code
gender
date_of_birth
phone_number
email
password
chronic_diseases
documents
address

    def register()
    def login()
    def update_profile()
    def view_medical_history()
```

```
class Doctor:
doctor_id
name
family
medical_id_number
specialty_id
phone_number
email
password
documents
approval_status

    def approve_doctor()
    def login()
    def view_patients()
```

```
class Specialty:
specialty_id
name

    def list_doctors_by_specialty()
```

```
class Appointment:
appointment_id
patient_id
doctor_id
types_of_appointments_id
date_time
status
video_link

    def schedule()
    def cancel()
    def update_status()
```

```
class TypeOfAppointment:
types_of_appointments_id
name
platform

    def get_available_types()
```

```
class VitalSign:
vital_id
patient_id
systolic_bp
diastolic_bp
heart_rate
blood_glucose
oxygen_saturation
temperature
measured_at

    def record()
    def fetch_latest()
```

```
class Prescription:
prescription_id
patient_id
doctor_id
diagnosis
notes

    def add_item()
    def get_prescription()
```

```
class PrescriptionItem:
item_id
prescription_id
drug_id
dosage
frequency
duration
```

```
class Reminder:
reminder_id
patient_id
drug_name
time_of_first_use

    def send_notification()
```

```
class EducationalContent:
content_id
title
content_type
file_url
average_rating

    def rate()
    def view()
```

```
class ContentFeedback:
feedback_id
content_id
patient_id
store
comment
submitted_at
```

```
class PharmacyOrder:
order_id
patient_id
prescription_id
pharmacy_id
order_status
order_date
tracking_code

    def place_order()
    def track_order()
```

```
class Pharmacy:
pharmacy_id
name
address
phone_number
delivery_available
location

    def get_location()
```

```
class Message:
message_id
sender_id
receiver_id
content
sent_at
seen

    def send()
    def mark_as_seen()
```

```
class Device:
device_id
device_type
model_name
serial_number
connection_type

    def connect()
```

```
class DeviceIsUsed:
device_is_used_id
device_id
patient_id
```

```
class Alert:
alert_id
patient_id
triggered_by
severity
sent_to
status

    def trigger()
    def mark_resolved()
```

```
class Consent:
consent_id
consent_type
signed_at
valid_until
signature_image
```

```
class ConsentPatient:
consent_patient_id
consent_id
patient_id
```

```
class SpecialistReferral:
referral_id
from_doctor_id
to_doctor_id
patient_id
reason
date_issued
accepted

    def accept()
```

```
class VideoSessionLog:
session_id
appointment_id
duration_in_minutes
connection_quality
issues_reported
recorded_url

    def log_session()
```

```
class VideoSessionLogDoctor:
session_id
doctor_id
patient_id
```

```
class PaymentTransaction:
transaction_id
patient_id
amount
purpose
transaction_date
payment_method
status

    def process()
    def refund()
```

```
class Drug:
drug_id
name
form
strength
usage_instructions

    def get_info()
```

```
class SymptomLog:
symptom_id
patient_id
vital_id
symptom_name
severity
logged_at
notes

    def log_symptom()
```

```
class SurveyDoctor:
survey_id
patient_id
doctor_id
text
```

```
class SurveyPharmacy:
survey_id
patient_id
pharmacy_id
text
```

```
class Factor:
factor_id
patient_id
type
status
```

```
class PaymentFactors:
patient_factor_id
factor_id
```

```
class Admin:
admin_id
name
family
phone_number
email
password
validated

    def login()
    def validate_account()
```

```
class Permission:
permission_id
name
```

```
class Role:
role_id
name
```

## Add

```
class Insurance {
    insuranceId
    name
    coverageDetails
    phone_number
    address
}
```

```
class InsurancePharmacy {
    id
    pharmacyId
    insuranceId
    contractStart
    contractEnd
}
```

```
class Disease {
    diseaseId
    name
    description
}
```

```
class Nurse {
    nurseId
    name
    family
    phoneNumber
    email
    licenseNumber
    password
    experienceYears
    gender
}
```

```
class HospitalizationAtHome {
    id
    patientId
    doctorId
    startDate
    endDate
    status
    notes
}
```
