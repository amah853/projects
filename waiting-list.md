# Waiting List Management System

This project is a Flask-based application for managing and displaying real-time waiting lists. It features an operator view for queue management and a public display view for sharing the list. Follow the steps below to install and use the system.
DOWNLOAD ZIP LINK - https://projects.ahmad-mahrous.com/waiting-list.zip

---

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Running the Application](#running-the-application)
4. [Using the Application](#using-the-application)
    - [Operator View](#operator-view)
    - [Public Display View](#public-display-view)
5. [Customization](#customization)

---

## Prerequisites

Before getting started, ensure you have the following installed on your machine:

- **Python 3.7+**
- **pip** (Python package installer)

---

## Installation

### Step 1: Download the ZIP and uncompress it.
You can find the download at https://projects.ahmad-mahrous.com/waiting-list.zip
Run the below command in your terminal:

```bash
cd waiting-list-system
```

### Step 2: Set Up a Virtual Environment (Optional)
It's recommended to use a virtual environment to keep dependencies isolated:

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
```

### Step 3: Install Dependencies
Install the required Python packages:

```bash
pip install -r requirements.txt
```

---

## Running the Application

### Step 1: Start the Flask Server
Run the application using the following command:

```bash
sudo python app.py
```

> **Note:** Port 80 requires superuser privileges; hence, use `sudo` if on a Unix-like system. *If you do not have superuser, you can try to run the command without sudo, it works on some computers.*

### Step 2: Access the Application
Once the server is running, you can access the application in your browser:

- **localhost Link:** `http://localhost/`

---

## Using the Application

### Operator View
The operator view is used to manage the waiting list:
1. Select a station from the dropdown menu.
2. Add names to the list, remove names, reorder items, or mark someone as a VIP (priority).
3. Changes are immediately reflected in the public display view.

### Public Display View
The display view shows the current waiting list for a selected station:
1. Select a station from the dropdown menu.
2. The list automatically updates every 100 milliseconds.
3. VIP tags are prominently displayed, and VIPs are always listed at the top.

---

## Customization

- **Stations:** You can configure the number of stations in the `app.py` file by modifying the `stations` dictionary.
- **CSS:** Modify `static/styles.css` to change the appearance of the application.
- **Port/Host:** Change the `host` and `port` in `app.run()` (default is `0.0.0.0:80`).

---

If you have any issues, email me at me@ahmad-mahrous.com!
