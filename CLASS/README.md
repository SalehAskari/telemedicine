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

````
class DoctorAvailableSlot:
    slot_id
    doctor_id
    types_of_appointments_id
    start_time
    end_time
    is_booked

    def mark_as_booked()
    def mark_as_available()
    def update_slot_time()
    def get_slot_details()
    ```
````

class Appointment:
appointment_id
patient_id
slot_id
status
video_link

    def book_appointment()
    def cancel_appointment()
    def join_appointment()
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
time_of_use
next_time_use
few_hours

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

```
class MedicalDocumentType:
mdt_id
name

    def create_type()
    def update_type()
    def delete_type()

```

```
class MedicalDocument:
medical_document_id
patient_id
file_url
mdt_id

    def upload_document()
    def update_document()
    def delete_document()
    def view_document()

```

```
class Hospital:
hospital_id
name
code
phone_number
email
address
city
province
hospital_type
website
description

    def register_hospital()
    def update_info()
    def get_details()

```

```
class RequestSendMedicine:
rsm_id
pharmacy_order_id
request_date
receiver_name
receiver_phone
delivery_address
delivery_location
preferred_time_window
delivery_cost
need_refrigerator
fast_delivery
notes
delivery_status_id

    def create_request()
    def update_request()
    def cancel_request()
    def track_delivery()

```

```
class DeliveryStatus:
delivery_status_id
name
description

    def set_status()
    def update_status()
    def get_status()
```

```
class SendMedicine:
send_medicine_id
snapp_tracking_code
name
phone_number
vehicle_model
vehicle_plate
national_id
profile_photo_url

    def assign_delivery()
    def update_driver_info()
    def complete_delivery()

```

```
class RoleChat:
    role_chat_id
    name

    def create()
    def update()
    def delete()

```

```
class User:
    user_id
    role_chat_id
    reference_id
    name
    profile_photo_url

    def join_chat()
    def send_message()
    def update_profile()
    def get_chats()

```

```
class Chat:
    chat_id
    is_group
    name
    created_by

    def create()
    def rename()
    def delete()
    def add_participant()
    def remove_participant()

```

```
class ChatParticipant:
    chat_id
    user_id
    role_chat_id
    joined_at

    def join()
    def leave()
    def update_role()

```

```
class Message:
    message_id
    chat_id
    sender_id
    content
    message_type
    reply_to_id
    sent_at
    edited_at
    deleted_at

    def send()
    def edit()
    def delete()
    def reply()

```

```
class MessageMedia:
    media_id
    message_id
    file_url
    file_type
    file_size

    def upload()
    def download()
    def delete()

```

```
class MessageStatus:
    message_id
    user_id
    is_seen
    seen_at
    is_delivered

    def mark_seen()
    def mark_delivered()
    def get_status()
```

```
class ReportNurse:
    report_id
    nurse_id
    patient_id
    vital_id
    shift
    status
    notes
    next_action

    def create_report()
    def update_report()
    def view_report()
    def delete_report()

```
