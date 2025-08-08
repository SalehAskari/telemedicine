# Entities

```
patients(patient_id, name, family, national_code, gender, date_of_birth, phone_number, email, password, chronic_diseases, documents, address)
```

```
doctors(doctor_id, name, family, medical_id_number, specialty_id, phone_number, email, password, documents, approval_status)
```

```
specialties(specialty_id, name)
```

```
available_appointments(available_appointment_id, doctor_id, types_of_appointments_id, start_time, end_time, is_reserved)
```

```
appointments(appointment_id, available_appointment_id, patient_id, status, video_link)
```

```
types_of_appointments(types_of_appointments_id, name, platform)
```

```
vital_signs(vital_id, patient_id, systolic_bp, diastolic_bp, heart_rate, blood_glucose, oxygen_saturation, temperature, measured_at)
```

```
prescription(prescription_id, patient_id, doctor_id, diagnosis, notes)
```

```
prescription_item(item_id, prescription_id, drug_id, dosage, frequency, duration)
```

```
reminder(reminder_id, patient_id, drug_name, time_of_first_use)
```

```
educational_content(content_id, title, content_type, file_url, average_rating, disease_id, specialty_id)
```

```
content_feedback(feedback_id, content_id, patient_id, store, comment, submitted_at)
```

```
pharmacy_order(order_id, patient_id, prescription_id, pharmacy_id, order_status, order_date, tracking_code)
```

```
pharmacy(pharmacy_id, name, address, phone_number, delivery_available, location)
```

```
device(device_id, device_type, model_name, serial_number, connection_type)
```

```
device_is_used(device_is_used_id, device_id, patient_id)
```

```
alert(alert_id, patient_id, triggered_by,severity, sent_to, status)
```

```
consent(consent_id, consent_type, signed_at, valid_until, signature_image)
```

```
consent_patient(consent_patient_id, consent_id, patient_id)
```

```
specialist_referral(referral_id, from_doctor_id, to_doctor_id, patient_id, reason, date_issued, accepted)
```

```
video_session_log(session_id, appointment_id, duration_in_minutes, connection_quality, issues_reported, recorded_url)
```

```
video_session_log_doctor(session_id, doctor_id, patient_id)
```

```
payment_transaction(transaction_id, patient_id, amount, purpose, transaction_date, payment_method, status)
```

```
drug(drug_id, name, form, strength, usage_instructions)
```

```
symptom_log(symptom_id, patient_id, vital_id, symptom_name, severity, logged_at, notes)
```

```
survey_doctor(survey_id, patient_id, doctor_id, text)
```

```
survey_pharmecy(survey_id, patient_id, pharmacy_id, text)
```

```
factors(factor_id, patient_id, type, status)
```

```
admin(admin_id, administrator, name, family, phone_number, email, password, validated)
```

```
permission(permission_id, name)
```

```
role(role_id, name)
```

```
admin_role(admin_role_id, admin_id, role_id)
```

```
admin_permission(admin_permission_id, admin_id, permission_id)
```

## Add

```
insurance(insurance_id, name, coverage_details, phone_number, address)
```

```
insurance_patient(insurance_patient_id, patient_id, insurance_id, policy_number, expiration_date)
```

```

support_insurance_pharmacy(support_insurance_pharmacy_id, pharmacy_id, insurance_id, contract_start, contract_end)
```

```
disease(disease_id, name, description)
```

```
nurse(nurse_id, name, family, phone_number, email, license_number, password, experience_years, gender)
```

```
hospitalization_at_home(hospitalization_id, patient_id, doctor_id, start_date, end_date, status, notes)
```

```
hospitalization_at_home_nurse(hhn_id, hospitalization_id, nurse_id, assigned_date, shift_time)
```

```
MedicalDocumentType(mdt_id, name)
```

```
MedicalDocument(medical_document, patient_id, file_url, mdt_id)
```

```
hospital(hospital_id, name, code, phone_number, email, address, city, province, hospital_type, website, description)
```

```
support_hospital_insurance(shi_id, hospital_id, insurance_id)
```

```
hospital_doctore(hospital_doctore_id, hospital_id, doctor_id)
```

```
request_send_medicine(rsm_id, pharmacy_order, request_date, receiver_name, receiver_phone, delivery_address, delivery_location, preferred_time_window, delivery_cost, need_refrigerator, fast_delivery, notes, delivery_status_id)
```

```
delivery_status(delivery_status_id, name, description)
```

```
send_medicine(send_medicine_id, snapp_tracking_code, name, phone_number, vehicle_model, vehicle_plate, national_id, profile_photo_url)
```

```
role_chat(role_chat_id, name)
```

```
users(user_id, role_chat_id, reference_id, name, profile_photo_url)
```

```
chat(chat_id, is_group, name, created_by)
```

```
chat_participant(chat_id, user_id, role_chat_id, joined_at)
```

```
message(message_id, chat_id, sender_id, content, message_type, reply_to_id, sent_at, edited_at, deleted_at)
```

```
message_media(media_id, message_id, file_url, file_type, file_size)
```

```
message_status(message_id, user_id, is_seen, seen_at, is_delivered)
```
