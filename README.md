# EmployeeManagementSystem
This program offers a versatile framework for employee management. Key classes include IncomeTax (IR), defining tax calculations, IEmployee as an employee base class, Employee for generic employees, Trainer with overtime features, and Agent with additional responsibilities.

# More details :
<b>1_ IncomeTax (IR):</b>

Abstract Base Class (ABC) representing Income Tax (IR). Defines income tax brackets, rates, and an abstract method to calculate income tax.
Attributes:
_tranches: List of income tax brackets. Each pair of elements represents the lower and upper limits of a bracket.
_tauxIR: List of corresponding income tax rates for each bracket.
Methods:
getIR: Abstract method to calculate income tax based on the provided salary.

<b>2_ IEmployee:</b>

Abstract Base Class (ABC) representing an employee. Defines three abstract methods - Age, Seniority, and RetirementDate - that any concrete class inheriting from it must implement.
Methods:
Age: Abstract method to calculate the age of the employee.
Seniority: Abstract method to calculate the years of service of the employee.
RetirementDate: Abstract method to calculate the retirement date of the employee.

<b>3_ Employee:</b>

Class representing a generic employee. Inherits from IEmployee and includes common attributes and methods for all employees.
Attributes:
_counter: Class variable to keep track of the total number of employees.
Methods:
salaireAPayer: Abstract method to calculate the salary to be paid.

<b>4_ Trainer:</b>

Class representing a Trainer. Inherits from Employee and IR, adding attributes specific to trainers (overtime hours and hourly rate).
Attributes:
__heureSup: Number of overtime hours.
__tarifHsup: Overtime hourly rate.
Methods:
salaireAPayer: Method to calculate the total salary, including overtime and income tax.

<b>5_ Agent:</b>

Class representing an Agent. Inherits from Employee and IR, adding an attribute specific to agents (primeResponsabilite).
Attributes:
primeResponsabilite: Responsibility bonus.
Methods:
salaireAPayer: Method to calculate the net salary, including responsibility bonus and income tax.
