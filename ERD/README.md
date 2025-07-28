# Entities

patients(patient_id, name, family, national_code, gender, date_of_birth, phone_number, email, password, chronic_diseases, documents, address)

doctors(doctor_id, name, family, medical_id_number, specialty, phone_number, email, password, documents, approval_status)

specialties(specialty_id, name)

appointment(appointment_id, patient_id, doctor_id, appointment_type, date_time, status, video_link)

types_of_appointments(types_of_appointments_id, name, platform)

vital_signs(vital_id, patient_id, systolic_bp, diastolic_bp, heart_rate, blood_glucose, oxygen_saturation, temperature, measured_at)

prescription(prescription_id, patient_id, doctor_id, diagnosis, notes)

prescription_item(item_id, prescription_id, drug_name, dosage, frequency, duration)

reminder(reminder_id, patient_id, drug_name, time_of_first_use)

educational_content(content_id, title, content_type, file_url, average_rating)

content_feedback(feedback_id, content_id, patient_id, rating, comment, submitted_at)

pharmacy_order(order_id, patient_id, prescription_id, pharmacy_id, order_status, order_date, tracking_code)

pharmacy(pharmacy_id, name, address, phone_number, delivery_available, location)

admin_user(admin_id, name, family, phone_number, email, password)

message(message_id, sender_id, receiver_id, content, sent_at, attachment_url)

device(device_id, patient_id, device_type, model_name, serial_number, connection_type, registered_at)

alert(alert_id, patient_id, triggered_by,severity, sent_to, status)

consent(consent_id, patient_id, consent_type, signed_at, valid_until, signature_image)

specialist_referral(referral_id, from_doctor_id, to_doctor_id, patient_id, reason, date_issued, accepted)

notification_log(notification_id, recipient_id, channel, message_text, status, timestamp)

video_session_log(session_id, appointment_id, duration_in_minutes, connection_quality, issues_reported, recorded_url)

payment_transaction(transaction_id, patient_id, amount, purpose, transaction_date, payment_method, status)

health_program(program_id, patient_id, title, start_date, end_date, goals, assigned_doctor_id)

login_audit(login_id, user_id, login_time, logout_time, ip_address, device_info, login_status)

error_log(error_id, module_name, error_message, stack_trace, occurred_at, severity, resolved_by)

support_ticket(ticket_id, user_id, subject, description, status, created_at, closed_at, assigned_admin_id)

tag(tag_id, tag_name)

content_tag(content_tag_id, content_id, tag_id)

drug(drug_id, name, form, strength, manufacturer, usage_instructions)

pharmacy_stock(stock_id, pharmacy_id, drug_id, quantity_available, price_per_unit, last_updated)

symptom_log(symptom_id, patient_id, symptom_name, severity, logged_at, notes)

document_upload(file_id, uploaded_by_user_id, file_name, file_type, upload_date, linked_entity_id)

survey(survey_id, title, target_group, created_at, is_active)

survey_response(response_id, survey_id, user_id, answer_data, submitted_at)

health_goal(goal_id, patient_id, title, start_date, target_date, progress_percentage)

users(user_id, name, family, phone_number, email, password, validated)

permission(permission_id, name)

role(role_id, name)
