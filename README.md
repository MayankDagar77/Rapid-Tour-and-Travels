# REST API for an Online Trip Management System

<img align="right" style="height: 200px;" src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8bmF0dXJlfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=600&q=60" alt="coding img">
![Alt text](https://github.com/MayankDagar77/Rapid-Tour-and-Travels/blob/main/Images/Rapid_Logo.jpeg)

- We have developed this REST API for an Online Trip Management System. This API performs all the fundamental CRUD operations of any Trip Management Application platform with user validation at every step.
- This project is developed by team of 3 Back-End Developers during project week in Masai School.

## Tech Stack

- Java
- Spring Framework
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
- PostMan
- Swagger
- Lombok

<p>
   <img src="https://img.icons8.com/color/64/000000/mysql.png" />
   <img src="https://img.icons8.com/color/64/000000/java.png" />
   <img src="https://logodix.com/logo/34937.png" alt="aws" width="60" height="60"/>
    <br> </br>
    
   <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="60" height="60" />
   <a>_</a>
   <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRbl9B2yl7iTuYk4JCAFSTuytuYidlQk_h4pmyt_1EJrwyyIsk5Qcwlh6q2_pbATZr2_lg&usqp=CAU" alt="laravel" width="60" height="60"/>
    <a>_</a>
   <img src="https://design.jboss.org/hibernate/logo/final/hibernate_logo_whitebkg_stacked_256px.png" alt="git" width="60" height="60" />
    <a>_</a>
   <img src="https://w7.pngwing.com/pngs/330/684/png-transparent-spring-framework-software-framework-model-view-controller-web-framework-java-pepper-robot-text-logo-opensource-software-thumbnail.png" alt="git" width="60" height="60" />
   <a>_</a>
   <img src="https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2.0,f_auto,g_center,h_1080,q_100,w_1080/v1/gcs/platform-data-dsc/events/spring-boot-1_5zDxm9B.jpg" alt="git" width="60" height="60" />
   
</p>

## Modules

- Login, Logout Module
- User Module
- Admin Module
- Booking Management Module
- Feedback Module
- Report Module
- Trip Package Management Module
- Route Mangement Module

## Features

- User and Admin authentication & validation using session uuid(key) and  @Valid annotation.
- Admin Features:
  - Administrator Role of the entire application where admin can be added or removed.
  - Only registered admins with valid session token(uuid) can add/update/delete Package,Hotel,Route or customer from main database.
  - Admin can access the details of different Routes, Bus, Packages, TicketDetails,Feedback,Customer,Reports,etc.
  - Only admin can generate reports.
- Customer Features:
  - A customer can register himself or herself on the platform.
  - User/Customer can check the Packages and Hotels availabilty.
  - If Trip Package is available, customer can book the trip package by providing payment details.
  - After booking, customer will get booking details for the whole Package inside this there will be all details regarding the ticket details ,total cost, etc.
  - Customer can cancel the booking.

## Contributors

- [@Mayank Dagar](https://github.com/MayankDagar77)
- [@Akshata Jinagond](https://github.com/akshatajinagond91)
- [@Yash Bhindia](https://github.com/yashbhindia)

## Installation & Run

- Before running the API server, you should update the database config inside the [application.properties](https://github.com/mrFarooque/rightful-order-9279/blob/main/TripManagementSystem/src/main/resources/application.properties) file.
- Update the port number, username and password as per your local database config.

```
    server.port=8888 // update it 

    spring.datasource.url=jdbc:mysql://localhost:3306/tmsdb;
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=root

```

ER diagram========= 

![image](https://user-images.githubusercontent.com/105930703/201670525-6a67228a-b2af-49db-a409-acf8e34595e2.png)

## API Root Endpoint

`https://localhost:8888/`

`http://localhost:8888/swagger-ui/`

## API Module Endpoints

### Login Module

- `POST //api/adminlogin` : Admin can login with mobile number and password provided at the time of registation
<!--

### User Module

- `POST /customer/login` : Logging in customer with valid mobile number & password
- `GET /customer/availablecabs` : Getting the list of all the available cabs
- `GET /customers/cabs` : Getting All the cabs
- `GET /customers/checkhistory` : Getting the history of completed tr
- `PUT /customer/update/{mobile}` : Updates customer details based on mobile number
- `PATCH /customer/updatepassword/{mobile}` : Updates customer's password based on the given mobile number
- `POST /customer/booktrip` : Customer can book a cab
- `POST /customer/updatetrip` : Customer can modify or update the trip
- `POST /customer/logout` : Logging out customer based on session token
- `DELETE /customer/delete` : Deletes logged in user
- `DELETE /customer/complete/{tripid}` : Completed the trip with the given tripid
- `DELETE /customer/canceltrip` : Cancel the trip with the given tripid

### Admin Module

- `POST /admin/register` : Register a new admin with proper data validation and admin session
- `POST /admin/login` : Admin can login with mobile number and password provided at the time of registation
- `GET /admin/logout` : Logging out admin based on session token
- `GET /admin/listoftripsbycustomer` : Get list of trips of by a customer id
- `GET /admin/listoftrips` : Get list of trips of all the trips
- `GET /admin/listocustomers` : Get list of all the customers
- `GET /admin/listodrivers` : Get list of all the drivers
- `PUT /admin/update/{username}` : Updates admin detaisl by passed user name
- `DELETE /admin/delete` : Deletes the admin with passed id -->

### Sample API Response for Admin Login

`POST localhost:8080/login/adminlogin`

- Request Body

```
    {
        "mobileNo": "888260649",
        "password": "Admin@123"
    }
```

- Response

```
   CurrentAdminSession(id=11, adminId=10, uuid=ZaVLaK, localDateTime=2022-08-17T11:13:42.772910500)

```

## Video Explainer of flow control

<a href="https://drive.google.com/drive/folders/1ktgjb8dRtgKQ5BCFNhBUr3BEzYLEeIdi?usp=sharing">**Video Drive Link** </a>

---

<img src=".\Images\ER_Diagram_TMS.jpeg" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### Swagger UI

---

![image](https://user-images.githubusercontent.com/105930703/202098886-e78cc7f3-ee5d-446f-864b-c36b736e2589.png)

---

### Login Controller

---

![image](https://user-images.githubusercontent.com/105930703/202099260-796ee7a9-f22d-48c0-b0c4-cb12d71f6627.png)

---

### Admin Controller

---

![image](https://user-images.githubusercontent.com/105930703/202099426-88f70611-5609-4e31-a474-98f40077ae31.png)

---

### Customer Controller

---

![image](https://user-images.githubusercontent.com/105930703/202099608-6ad56ed9-ff48-405b-9b36-fff1529182b8.png)

---

### Model Controller

---

![image](https://user-images.githubusercontent.com/105930703/202099802-8e5dcf6b-8974-454b-94fa-f0e049d1827f.png)

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/Thank-you-word-cloud.jpg?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---
