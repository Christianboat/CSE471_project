








BRAC University 
Summer 2024 
StyleNest Appointment Booking & Beauty Products Management System


CSE471: System Analysis and Design Lab
Group 8 -  Section 2

Group Member’s Information: 
Student ID
Student Name
22101816
Christian Boateng
20101167
Kazi Shashwata Rahman
21201541
Ifaz Ibne Baten


Tsewang Choden






Table of Contents
Introduction
Technology Used
User Manual
Frontend Development Explanation
Backend Development Explanation
GitHub Repository Link
Individual Contribution


1. INTRODUCTON

Project Story:
Beauty establishments can make appointments using StyleNest. Customers can use this platform to sign up, log in, schedule appointments, and place orders for beauty products. All employees can also register, log in, process or cancel orders, and check the status of services using this system. The goal of this project is to efficiently manage salon services, enhance customer interaction, and handle sales of beauty products.






2. TECHNOLOGY USED

Frameworks
Frontend: Bootstrap
Backend: Django
Languages:
HTML
CSS
JavaScript
Version control
Git & Github



3. USER MANNUAL


How to Run the Project

System Requirements
Python 3.8 or higher
Django 3.2 or higher
Any web browser
Setup Instruction
Clone the GitHub repository:
git clone [repo-link]
cd StyleNest
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
Open the browser at http://localhost:8000 to interact with the system.

How to Use the System
For Customers:
Register or Login
Browse the available services and beauty products
Book an appointment
Place orders for hair products
For Staffs
Login in to the staff dashboard
Register with email of @stylenest.com
View, accept or cancel appointments
Manage the orders of customers: view accept and cancel orders.


4. FRONEND DEVELOPMENT EXPLANATION 

Homepage
Navigation bar provides link to to view the services, and login or register.
Display of animation of services and a book button which takes you to the login paage.









User Authentication (Login/SignUp)
An integrated Django authentication system for staffs and user to login
Users can sign up and Staffs can also sign up with their email @stylenest.com





3.  Customer Home Page
A top navigation bar that contains the current date and the logout button
A right sided navigation bar that displays the appointmensts of the user (services, subservice, date, time, and the status of the appointment)
A left saided navigation bar with the iframe links of the customer dashboard, appointment booking, products, cart and the orders of the user
An ifram that displays the content of the links in the left sided navigation bar


Customer Home Page Book
Customers can select available services of their choice, choose a time slot and then confirm the booking



Customer Home Page Products
Customers can see all listed products




Customer Home Page Products View Products
Customers can view the product when clicked on the view on any product






Customer Home Page Cart
Customers can view the cart and checkout the items in the cart




Customer Home Page Cart Checkout
Customers can checkout all the products added to the cart



Customer Home Page My Oders
Customers can see their orders and the status of the order.

4.  Staff Home Page
A top navigation bar that contains the logout button
A right sided navigation bar that displays the appointmenst requests
A left saided navigation bar with the iframe links of the customers appointment lists,  and orders.
An ifram that displays the content of the links in the left sided navigation bar




StaffHome Page Appointments
Staff can see all appointments and choose to either accept or reject.




StaffHome Page Orders
Staff can see all orders, accept the order, prepare it, deliver and cancel.



Logic and Uscase Explanation
User role based access control
The built-in authentication system of Django is utilized to access control. The customers have access to only the customer dashboard while the staffs also have access to the staff dashboard
State management
The session based authentication of django handle the user data while ensuring a secure and consistant interaction with the system.




5. BACKEND DEVELOPMENT EXPLANATION 

User Authentication
POST/api/login: This validate their credentials, both customers and staffs and gives them access to the system
POST/api/registe: this registers new users, both customers and staffs allowing them to sign up and store their credentials in the system’s database.
Appointments
POST/api/book: This allows users to book appointments. It handles appointment inputs like the service , sub-service, date, time etc and store them in the database.
GET/api/appointments: this retrieves appointments based on the users role. Custometrs can see their own appointments (pending, confirmed, canceled).Stafss on the other hand can see their accepeted appointments
PUT/api/appointments/:id/cancel : customers can cancel appointments if the status is confirmed.
Orders Management
POST/api/orders : customers can place orders for a product. The system takes the details and store it in the database.
GET/api/orders : retrieves all orders place by the customer and then seen by staffs. Customers can see their orders while staff can also view the orders to manage the order processing
Product Management
GET/api/products: This allows customers to see available products and its description before placing the order. And also retrieve detail information on a specific product.

Logic and Usecase Explanation
Django Model and Bussiness Logic
Accounts Model: separate models for staffs and customers with role based permissions
Appointments Model: Stores appointment details such as services, subservices, date and time
Service Model: Stores the services and subservices that the business offers to customers
Shop models: Store the products and their descriptions. Also saves the order details of the customers.
Django ORM
 A simplified database interactions. Appointments and oders are fetched and updated through the ORM queries ensuring an operation that is fast and reliabe 
Admin panel
 This is used by the administrator to manage the services, appointments , user accounts and orders.


6. Github Link


















6. Individua Contributions

CHRISTIAN BOATENG
Kazi Shashwata Rahman
Ifaz Ibne Baten
Tsewang Choden
Front ends
Shop Module
 Accounts  Module
Website Idea
Appointment Module




Suggested all the functionalities of the website


