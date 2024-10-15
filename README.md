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

1NF: Each table has atomic columns.
2NF: No partial dependency of non-prime attributes on candidate keys.
3NF: No transitive dependencies between non-prime attributes.
Example: ARTIST Table
Functional Dependency: ARTIST_ID -> ARTIST_NAME, COUNTRY, DOB
Normalization: The table is in 3NF because it has no transitive dependencies.
