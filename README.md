# HOSPITAL-MANAGEMENT-SYSTEM-PYTHON-PROJECT
# Simple Hospital Management System (Beginner Level)

patients = []
doctors = []
appointments = []

def add_patient():
    print("\n--- Add Patient ---")
    name = input("Enter patient name: ")
    age = input("Enter age: ")
    gender = input("Enter gender: ")
    phone = input("Enter phone number: ")
    
    patient = {
        "name": name,
        "age": age,
        "gender": gender,
        "phone": phone
    }
    patients.append(patient)
    print("Patient added successfully!")

def add_doctor():
    print("\n--- Add Doctor ---")
    name = input("Enter doctor name: ")
    spec = input("Enter specialization: ")
    
    doctor = {
        "name": name,
        "specialization": spec
    }
    doctors.append(doctor)
    print("Doctor added successfully!")

def make_appointment():
    print("\n--- Make Appointment ---")
    patient_name = input("Enter patient name: ")
    doctor_name = input("Enter doctor name: ")
    date = input("Enter appointment date: ")

    appointment = {
        "patient": patient_name,
        "doctor": doctor_name,
        "date": date
    }
    appointments.append(appointment)
    print("Appointment created!")

def view_patients():
    print("\n=== All Patients ===")
    for p in patients:
        print(p)

def view_doctors():
    print("\n=== All Doctors ===")
    for d in doctors:
        print(d)

def view_appointments():
    print("\n=== All Appointments ===")
    for a in appointments:
        print(a)

# -------------------------
# Main Menu
# -------------------------

while True:
    print("""
========= HOSPITAL MANAGEMENT =========
1. Add Patient
2. Add Doctor
3. Create Appointment
4. View Patients
5. View Doctors
6. View Appointments
0. Exit
""")

    choice = input("Enter choice: ")

    if choice == "1":
        add_patient()
    elif choice == "2":
        add_doctor()
    elif choice == "3":
        make_appointment()
    elif choice == "4":
        view_patients()
    elif choice == "5":
        view_doctors()
    elif choice == "6":
        view_appointments()
    elif choice == "0":
        print("Exiting... Goodbye!")
        break
    else:
        print("Invalid choice! Try again.")
