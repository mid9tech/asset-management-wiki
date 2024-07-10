# 1 Overview

## 1.1 Goal
- Allows Admin to manage company’s assets
- Allows users to request to return an assignment

## 1.2 Brief Description
The asset management application is designed to help organizations manage their assets efficiently. It comprises a front-end built with Next.js, a back-end powered by NestJS, and utilizes various services such as Docker, Azure Container Registry, and Prisma for database management. The entire system is deployed and maintained using Azure services to ensure scalability, security, and reliability.

# 2 Actors and Scope

## ![image.png](/.attachments/image-e1a4b704-651d-4aa0-8686-16afb64ca1aa.png)

# 3 Preconditions
The actor must be signed in to the system.

# 4. Flow of Events

## 4.1 Manage User
###Basic flow - Log in/Log out
![image.png](/.attachments/image-0eb3c01e-21d0-4526-8f64-eb7408385207.png)


### Alternative Flow – Change password
![image.png](/.attachments/image-8b269e81-27bb-46a8-bf06-cc9a520c070e.png)


### Alternative Flow – Create new user
![image.png](/.attachments/image-73ca68fc-63eb-4a2a-bb8f-8c17ad59cc91.png)

### Alternative Flow – Edit user
![image.png](/.attachments/image-d9a47492-490b-46a3-936a-4c246e53e58f.png)

### Alternative Flow – Delete User
![image.png](/.attachments/image-2a803716-c8ad-41db-af77-12c21d498d6d.png)

### Alternative Flow – View user list
![image.png](/.attachments/image-a460fbf4-4466-4ede-92ac-1c014fd45d94.png)

## 4.2 Manage Asset

### Alternative Flow – Create new Asset
![image.png](/.attachments/image-e79b6273-125a-4cf3-a2c8-9870cda91dc4.png)

### Alternative Flow - Edit Asset
![image.png](/.attachments/image-a8b7d0c2-86e6-44a7-af29-3266adedb973.png)

### Alternative Flow – Delete Asset
![image.png](/.attachments/image-21fab5f0-3032-48a3-b6af-bb83099e8bc6.png)

### Alternative Flow – View Asset list
![image.png](/.attachments/image-25baa2da-35c0-46d9-bd10-00a9c15a1da8.png)

## 4.3 Manage Assignment

### Alternative Flow – Create new Assignment
![image.png](/.attachments/image-99f2ab8d-462d-44f6-9f37-c0a6a59588c8.png)

### Alternative Flow - Edit Assignment
![image.png](/.attachments/image-f2ee332f-d5b0-48d6-95dc-8268addd8c51.png)

### Alternative Flow – Delete Assignment
![image.png](/.attachments/image-926026a6-4a92-4aef-a765-ca233ef49145.png)


### Alternative Flow – View Assignment list
![image.png](/.attachments/image-03fb41a2-3102-4038-b7e8-6167aab03875.png)

## 4.4 Manage Request for Returning
### Alternative Flow – View Request for Returning list
![image.png](/.attachments/image-92de5d64-8ee4-4e57-bfc1-6c2057cfeda0.png)


### Alternative Flow – View Request for Returning list
![image.png](/.attachments/image-b8739fb3-dd9e-43b2-851e-a7a3ebad4084.png)

## 4.5 Asset Report
### Alternative Flow – View/Export Asset report
![image.png](/.attachments/image-29cc2b8c-6939-43d5-a8d6-0ddb33684161.png)
