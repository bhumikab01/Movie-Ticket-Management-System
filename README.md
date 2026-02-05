# Movie Ticket Management System: Project Overview

This project is a Python-based console application designed to manage movie listings and ticket bookings. It utilizes a MySQL backend to persist data and incorporates data visualization tools to track ticket sales trends.

## 🌟 Key Features

* **Dual-Portal System**:
    * **Admin Portal**: Securely accessible via password (`web@portal`). Admins can manage the movie database (Add/Delete/Show movies), view all booked tickets, and generate analytical graphs.
    * **User Portal**: Allows customers to book new tickets, view their existing bookings using a customer ID, or cancel a ticket.
* **Database Automation**: Upon starting with the correct PIN (`1234`), the system automatically initializes the `movtkt` database and creates tables for movies (`mt`) and bookings. It also populates the system with default movie and booking data if the tables are empty.
* **Data Visualization**:
    * **Line Graphs**: Displays a trend of tickets sold per movie.
    * **Bar Graphs**: Provides a visual comparison of ticket sales across different movie titles using `matplotlib`.
* **Automated Calculations**: Uses `pandas` DataFrames to organize and display database records in a clean, tabular format for both admins and users.

## 🛠️ Technology Stack

* **Language**: Python.
* **Database**: MySQL (connected via `mysql-connector-python`).
* **Data Analysis**: `pandas`.
* **Visualization**: `matplotlib.pyplot`.

## 📁 Project Structure

* `project.py`: The main script containing all functional logic, including database initialization, portal menus, and CRUD operations for movies and tickets.
* `README.md`: Basic project identification.
* `bookings.csv`: (Referenced in code) External data source used specifically for generating graphs.

## 🚀 Getting Started

1.  **Prerequisites**:
    * Python 3.x installed.
    * MySQL Server running on `127.0.0.1` at port `3307`.
    * Install dependencies:
        ```bash
        pip install mysql-connector-python pandas matplotlib
        ```
2.  **Configuration**:
    * Open `project.py` and ensure the MySQL `password` matches your local environment.
3.  **Run the Application**:
    ```bash
    python project.py
    ```

## 📝 Usage

* **Authentication**: Enter the system PIN `1234` to access the main menu.
* **Booking**: Users must provide details including Name, Address, Phone Number, Movie Code, and the Number of Tickets.
* **Admin Tasks**: Use the Admin portal to update the movie lineup or view the sales performance via the "Show Graph" option.
