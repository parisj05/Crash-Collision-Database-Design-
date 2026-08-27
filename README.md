# NYC Motor Vehicle Collision Database

## Overview

This project develops a relational database for analyzing motor vehicle collisions in New York City. The database organizes collision information, vehicles, drivers, vehicle types, vehicle makes, occupants, contributing factors, pre-crash conditions, and vehicle damage into related tables.

The goal of the project is to create a structured database that can be used to analyze traffic trends, identify contributing factors, and support research into road safety.

## Project Objectives

- Organize motor vehicle collision data into a relational database
- Apply database normalization and relational database design principles
- Maintain data integrity using primary and foreign keys
- Clean and prepare datasets for SQL import
- Create SQL views for analyzing collision trends and vehicle information
- Use joins, filtering, aggregation, and subqueries to answer analytical questions
- Create a database structure that can be expanded with additional datasets

## Database Schema

The database follows **Third Normal Form (3NF)** to reduce duplicate data and improve data consistency. Primary and foreign keys establish relationships between the database tables.

![NYC Motor Vehicle Collision Database ERD](images/database-erd.png)

## My Contributions

- Designed and normalized the relational database structure
- Cleaned and prepared datasets for SQL import
- Created tables with primary and foreign key relationships
- Developed SQL views using joins, filtering, aggregation, and subqueries
- Validated relationships and maintained referential integrity
- Documented database design decisions and data-cleaning challenges

## Data Preparation

The project uses CSV and Excel datasets to populate the database tables.

Data preparation included:

- Handling missing values
- Converting blank fields to SQL `NULL` values
- Preparing datasets for database import
- Maintaining referential integrity
- Organizing data according to the relational database design

Data was imported in a specific order to respect foreign key dependencies. Parent and lookup tables were loaded before dependent tables.

## SQL Analysis

Several SQL views were created to demonstrate different analytical techniques.

### `collisions_driver_vehicle_info`

Combines collision, driver, vehicle, vehicle make, and vehicle type information using multiple joins. The view focuses on collisions from 2020 onward.

**Techniques:** `JOIN` · `WHERE` filtering

### `yearly_collision_counts`

Counts the number of collisions occurring each year to identify trends over time.

**Techniques:** `GROUP BY` · `COUNT` · join table

### `top_contributing_factors`

Identifies the most common contributing factors associated with collisions and connects them with pre-crash information.

**Techniques:** `JOIN` · filtering · aggregation

### `vehicle_damage_details`

Combines vehicle, damage, vehicle make, and vehicle type information to provide detailed information about vehicle damage.

**Techniques:** `JOIN` · join tables

### `collisions_above_average_damage`

Identifies collisions involving more vehicle damage than the overall average.

**Techniques:** `JOIN` · aggregation · subquery

## Technologies Used

- **MySQL**
- **SQL**
- **Microsoft Excel**
- **CSV**
- **Relational Database Design**
- **Entity Relationship Modeling (ERD)**

## Repository Structure

```text
CRASH-COLLISION-DATABASE-DESIGN/
│
│
├── SQL/
│   ├── motor_vehicle_collisions.sql
│   ├── motor_vehicle_contributing_factors.sql
│   ├── motor_vehicle_driver.sql
│   ├── motor_vehicle_pre_crash.sql
│   ├── motor_vehicle_public_property_damage.sql
│   ├── motor_vehicle_vehicle_damage.sql
│   ├── motor_vehicle_vehicle_make.sql
│   ├── motor_vehicle_vehicle_occupant.sql
│   ├── motor_vehicle_vehicle_type.sql
│   └── motor_vehicle_vehicle.sql
│
├──
│   └── database-erd.png
│
├── Final Project Report.pdf
└── README.md
