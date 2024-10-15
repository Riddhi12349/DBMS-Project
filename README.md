# Music Library Database Management System

A PL/SQL-based project designed to manage a personal music library, including artists, albums, and tracks. This system can store, retrieve, and manage the details of a music collection using various database functionalities such as triggers, cursors, and stored procedures.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Database Structure](#database-structure)
6. [Code Examples](#code-examples)
    - [Insertion](#insertion)
    - [Deletion](#deletion)
    - [Triggers](#triggers)
7. [Normalization](#normalization)
8. [Contributors](#contributors)
9. [License](#license)

## Introduction

The Music Library database is designed to store details of a personal music collection, including:
- Artists
- Albums
- Tracks

This database can manage MP3, CD, or vinyl collections and handle tasks like inserting, updating, and retrieving music data. The system can handle data normalization, cursors for data retrieval, and triggers for automated actions.

## Features

- **Basic CRUD Operations**: Create, read, update, and delete entries for artists, albums, and tracks.
- **Normalization**: The database is normalized up to the 3rd Normal Form (3NF) for optimal structure.
- **Triggers**: Automated responses to database actions such as insertion and deletion.
- **Cursors**: Efficient data retrieval using cursors to manage tracks and albums.
- **Custom Functions and Procedures**: Includes error handling and logic encapsulated in PL/SQL functions and procedures.
- **Award Management**: Store and manage awards received by artists for specific tracks.

## Installation

To set up the Music Library Database:

1. Install a relational database system such as Oracle Database.
2. Create the required tables using the provided SQL scripts.
3. Run the PL/SQL procedures for data manipulation.

### ER DIAGRAM

![{87C8FA92-5F59-4494-B493-EB2425AEEA0B}](https://github.com/user-attachments/assets/d29b428f-cb84-4919-8b5e-7ad258f981f2)

## Usage

### Creating the Database

Run the following script to create the necessary tables:

sql
CREATE TABLE ARTIST(
    ARTIST_ID NUMBER PRIMARY KEY,
    ARTIST_NAME VARCHAR2(23),
    COUNTRY VARCHAR2(23),
    DOB DATE
);

### Insertion
To insert data into the database, you can use stored procedures like the following:
![{F0BC9458-E833-459B-A3A7-DFB22D09F370}](https://github.com/user-attachments/assets/42dd0135-d9e1-4e10-bd88-19a7f42bd041)

### Deletion
You can delete records using the custom deletion procedure with exception handling:
![{A5836F63-992E-4E25-B5E7-344FA2BA9390}](https://github.com/user-attachments/assets/cc675247-2c8b-4761-903f-13d2b6967d18)

### Database Structure
The database consists of the following key tables:

![{45BF66BA-A05C-4384-B8C4-58B6702D08EF}](https://github.com/user-attachments/assets/c1d6319d-bce1-4fed-b202-adeb2387d20c)
![{6554D6B4-FEC5-4609-A549-CC8883657134}](https://github.com/user-attachments/assets/9189c9f6-6352-40f6-8ce8-054a94a5cd48)
![{70C08FFA-AACC-4473-BE57-51B5F3252B64}](https://github.com/user-attachments/assets/efa2f7d9-8f04-48d2-92fb-28da97978ec9)


### Code Examples

#### Insertion
![{899CD63A-F329-400E-BB77-29864E6000CD}](https://github.com/user-attachments/assets/33b5083e-b46f-4f7a-b3b6-fa05b215cdfa)

#### Deletion
![{C2573614-E3A3-45FB-ADC3-F988FBBF2975}](https://github.com/user-attachments/assets/543129c8-4d1e-4f3f-ae75-6895707cb608)

### Triggers
To automatically respond to updates or deletions:
![{3BF7C018-936A-4D6E-8628-3BB7AB8D786A}](https://github.com/user-attachments/assets/02ff0e7b-89f7-4408-b31f-c8de7887593b)

### Normalization
![{B25FF013-6A9F-49EA-A0B0-DE0708A0A765}](https://github.com/user-attachments/assets/45ddd55e-1e8a-46d5-8564-d233abfce6d0)

#### Track
![{4843ABAA-77F9-463C-A358-2BD5F4FF22CB}](https://github.com/user-attachments/assets/e1e4e2c3-6fa2-4a16-a333-e3946e54f0c3)
![{57192530-FEF6-4436-8991-F0EF215D6251}](https://github.com/user-attachments/assets/4b8a1933-7e6b-4124-92b9-c48d4b548f3a)
![{1F037956-3B48-4238-A8FE-4A9244968912}](https://github.com/user-attachments/assets/559049a1-1e56-4016-ab9f-95ba1e4617e9)
![{50481542-B8E8-498F-938D-4C3B6ACA8D23}](https://github.com/user-attachments/assets/689cc601-cebf-492d-a3f3-2d40c8c673ca)
![{053CEF04-D7C3-493D-8066-4EACE8988307}](https://github.com/user-attachments/assets/7dcacd4f-e6b9-491b-afb2-1548d2d11f73)
![{F8FD458D-BBC9-4CCD-8E8D-988793EF9757}](https://github.com/user-attachments/assets/d26b8f3d-21bb-4bef-b381-7f81f4dd3428)
![{1EDA1FBF-804B-4893-9585-C541EB8E1BBD}](https://github.com/user-attachments/assets/942e4e39-d1c5-4c8a-9a62-ee47f598a902)
![{05038410-3CA3-4BB4-8F6C-3C2CF67F8CB8}](https://github.com/user-attachments/assets/fea9ad04-f318-4a99-b619-912b8e498def)
![{464D7068-4EA5-4A25-B7ED-66DA8945102F}](https://github.com/user-attachments/assets/6263907e-48b3-456d-a977-658ca0cfdc27)
![{FA663C5D-9CEC-49A0-8001-D3691DFBE215}](https://github.com/user-attachments/assets/f7c89247-dcec-47be-9601-3d8278ca3ce1)
![{211D4637-5B2B-4BC6-B252-B52F65CDFEEA}](https://github.com/user-attachments/assets/a93f1eb3-06af-440d-aac0-3eed87f0c9dd)
![{C45CD969-2308-4A2C-9F0D-FE7E99248242}](https://github.com/user-attachments/assets/b76aa7c3-317d-4a33-9af1-887485b24a37)
![{3CDD6140-8CB6-4D30-9C21-98E2306639EE}](https://github.com/user-attachments/assets/99a08c69-fb78-4970-8fbd-2bb8e901b5b4)
![{F2929626-988E-47A1-A664-D1C9881F9686}](https://github.com/user-attachments/assets/de0a0d35-5b45-4d33-9126-56820fdd8fac)
![{9D8BE984-D66C-4B51-A506-B5608713A5F5}](https://github.com/user-attachments/assets/d8e880c1-4a8c-4b1b-9830-5233598f1624)
![{E236D676-486A-400F-9EE5-F736A25577BE}](https://github.com/user-attachments/assets/fb3416b8-b111-4aee-965d-78d9b738dd5d)
![{8C26D47D-2D1F-4AE9-B9C6-4726386C61F9}](https://github.com/user-attachments/assets/63fe6c0c-6ede-437e-a5d5-a50c9df42c43)
![{D958F594-416B-450E-BFD2-35021DEED386}](https://github.com/user-attachments/assets/dabb73e4-68e7-4551-b0e4-7c4ac4700f6c)
![{E1526371-98EB-4906-B52E-717818AF3153}](https://github.com/user-attachments/assets/3fcd71b2-4c3c-403d-8874-845aa08a5fb8)
![{ADD873FB-FBA9-4AB2-A02A-3326A4D7A602}](https://github.com/user-attachments/assets/36ebee07-38a9-4f1b-bd43-d34b986f48d3)
![{38017B5A-77E9-4B9C-AFAB-133D779ED278}](https://github.com/user-attachments/assets/755c203c-7734-448c-876a-5dced67aae98)
![{5E58F983-5AC9-48CD-B944-DF8A69EB7C42}](https://github.com/user-attachments/assets/563dc575-dfc8-457f-b972-549b6d9f03a8)
![{FB9C130E-64A9-4F3A-B702-17A5287E06B5}](https://github.com/user-attachments/assets/1638fd33-a805-4ec1-ab32-7922d02cab54)




















