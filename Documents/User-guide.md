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
![image.png](/.attachments/image-ef97272a-6aac-4322-89dc-dd4ce4a95d68.png)


### Alternative Flow – Create new user
![image.png](/.attachments/image-73ca68fc-63eb-4a2a-bb8f-8c17ad59cc91.png)

### Alternative Flow – Edit user
![image.png](/.attachments/image-c62c2510-d23d-4311-af04-91cbfaa6e2e9.png)
### Alternative Flow – Delete User
![image.png](/.attachments/image-7c3a9d24-62cf-4eff-9031-299f62a0ebe7.png)
### Alternative Flow – View user list
![image.png](/.attachments/image-0e1fcec5-8cc9-48ae-8d7f-d2171dfd8c15.png)
## 4.2 Manage Asset

### Alternative Flow – Create new Asset
![image.png](/.attachments/image-e79b6273-125a-4cf3-a2c8-9870cda91dc4.png)

### Alternative Flow - Edit Asset
![image.png](/.attachments/image-157acc35-2337-4744-90ab-971c0e1d6b51.png)
### Alternative Flow – Delete Asset
![image.png](/.attachments/image-314945dd-ad98-446b-96dd-47dc33b58605.png)
### Alternative Flow – View Asset list
![image.png](/.attachments/image-62da03ea-fa2a-4dc7-8549-f206975cfc5d.png)

## 4.3 Manage Assignment

### Alternative Flow – Create new Assignment
![image.png](/.attachments/image-99f2ab8d-462d-44f6-9f37-c0a6a59588c8.png)

### Alternative Flow - Edit Assignment
![image.png](/.attachments/image-25d9e14f-45e3-4e48-b6a8-a9757a374080.png)

### Alternative Flow – Delete Assignment
![image.png](/.attachments/image-e607134e-a7f2-4523-ae6b-0c9329f34c29.png)

### Alternative Flow – View Assignment list
![image.png](/.attachments/image-7ae0f478-8697-41f6-80e0-499347534a94.png)

## 4.4 Manage Request for Returning
### Alternative Flow – Create Request for Returning list
![image.png](/.attachments/image-c9e9fc3a-3e3c-433b-9137-9866aa27dd60.png)


### Alternative Flow – View Request for Returning list
![image.png](/.attachments/image-11578e96-8f60-47da-909b-413fca7391a7.png)

## 4.5 Asset Report
### Alternative Flow – View/Export Asset report
![image.png](/.attachments/image-b46c36b3-349f-4a7c-8328-d3960f35fd62.png)
