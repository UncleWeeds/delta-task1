# delta-task1

Gamma Z Hostel & Mess Management Server

Normal Mode:
(alias - genStudent) Create an account for the HAD (Hostel Admin) with their own Home directory. Create respective accounts and Home directories for the Hostel Wardens and the Students. The Home directory names of the Hostel Wardens should be the names of their respective hostels. We will have directories for each Room within the Hostel directory numbered as 001 to ..., inside which we'll have the 2 Students home directories.

If a file is passed through the command line, set up the accounts as present in the file (studentDetails.txt can be used), else if no file is passed, take details as input from the user during run time and setup accounts accordingly.
Students should have a userDetails.txt and fees.txt present in their home directory. userDetails.txt should have Name, Roll Number, Department, Year, Hostel, Allocated Mess, Month, and Mess Preferences. fees.txt will have fee details (see feeBreakup alias below for file structure)
announcements.txt (the announcements of that hostel) and feeDefaulters.txt (the list of people who haven't paid fees) files are present in each Hostel directory.
The HAD will have a mess.txt (the initial file is provided with the same name).
Note: Use studentDetails.txt and mess.txt

(alias - permit) Set up permissions for accounts which follow the hierarchy:
Students should not be able to view any files outside their own home directory (except the announcements and feeDefaulters of their respective hostel).
Hostel wardens should be able to view and edit files of all the students belonging to that hostel but not of any other hostel.
HAD should be able to view and edit all the files.
All the students should be able to edit the mess.txt file.

(alias - updateDefaulter) The hostel warden can run this to read through the fee files of all the students of their hostel and check if the fee is paid before the end of the semester. If not, it adds an entry to the feeDefaulters.txt with their name and roll number. In order to encourage timely fee payment, the institute has decided to put up the roll numbers of the first 5 students from each hostel who paid fees in the announcements.txt of the respective hostel.

(alias - messAllocation) If a student runs this alias, they should be able to record their mess preference order in their userDetails.txt file as numeric sequence (each mess having an associated number) and the roll number should be appended to mess.txt. If this alias is run by the hostel office, all the students should be allocated messes according to the mess capacity (stored at the top of mess.txt) and preferences of students based on the time of filling preference.

(alias - feeBreakup) Students can pay the fees with this alias. Each student will have a percentage breakup of fees, provided by feeBreakup.txt and whenever they pay fee, the fees.txt file will be updated with the cumulative amount for each category at the top of the file and the transaction will also be appended each time it happens, in the same file.
SuperUser Mode:

(alias - signOut) Whenever a student wishes to stay out of campus overnight, they need to get an approval from the warden of their hostel. When a student runs this alias, the warden should be asked for confirmation. If approved, whenever the student returns (next log-in), it checks if it is before the provided return date.
