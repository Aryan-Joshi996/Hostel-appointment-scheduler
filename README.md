Features:
Add Appointment (Option 1): Books a new appointment by taking details like patient name, doctor name, date, time, and reason. 
It includes a basic check to prevent double-booking a single doctor at the same time and date.
View All Appointments (Option 2): Lists all scheduled appointments in the system.
View Appointments by Date (Option 3): Prompts the user for a specific date and lists only the appointments scheduled for that day.
Cancel Appointment (Option 4): Displays all appointments, prompts the user to select an appointment number, and removes the chosen appointment from the list.
Exit (Option 5): Terminates the program.
Data Storage: appointments = []
All appointments are stored in a global Python list called appointments.
Each appointment itself is stored as a dictionary within this list, with keys like "patient", "doctor", "date", "time", and "reason".
Main Loop: main()
The main() function contains a while True loop that continuously displays the main menu and prompts the user for a choice until option '5' (Exit) is selected.
It uses if/elif/else statements to call the relevant functions based on the user's input.
Key functions:
add_appointment()	Creates and adds a new appointment.
Includes a loop to check if the doctor is already booked at the proposed date and time, preventing conflicts.
list_appointments()	Displays all booked appointments.	
Iterates through the appointments list and uses an string to format and print the details with a sequential number.
list_appointments_by_date()	Displays appointments for a specific date.
Uses a list comprehension to efficiently filter the appointments list for the matching date.
cancel_appointment()	Removes a scheduled appointment.	
Calls list_appointments() first, takes a numbered input, and uses .pop(n - 1) to remove the correct appointment (adjusting for 0-based indexing).
It includes basic try-except for error handling if a non-number is entered.
To run this scheduler:
Save the code as a Python file (e.g., scheduler.py).
Open your terminal or command prompt.
Run the command: python scheduler.py
Follow the on-screen menu instructions.
