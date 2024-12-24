# Movie Theater System - Setup Instructions

A web application for managing RFID-based movie passes. Download at https://projects.ahmad-mahrous.com/theatre-management.zip

## Features

1. **Box Office**: Assign RFID tags to movies, with override functionality.
2. **Pass Checker**: Validate RFID tags for specific movies, with success/error messages.
3. **Manager**:
   - Add or remove movies.
   - Check which movie a tag belongs to.
   - End all active movie passes.
   - Manage staff accounts (add/update/remove).
   - Manage specific account role(s)
4. **User Authentication**: Restrict access based on user roles (`box_office`, `pass_checker`, `manager`).

---

## Prerequisites

- Python 3.7 or later
- SQLite3
- Flask
- Flask-Login
- A web browser
- Access to host on port 80 on your network (can be changed, but 80 is recomended)

---

## Setup Instructions

### 1. Download the Project ZIP, uncompress it, then cd into the directory
```bash
cd theatre-management
```

### 2. Install Required Packages
Install the dependencies using `pip`:
```bash
pip install flask flask-login
```

### 3. Create the Databases
1. Create the authentication database for user management:
   ```bash
   python create-auth-db.py
   ```
2. Create the movie theater database:
   ```bash
   python create-theater-db.py
   ```

### 4. Start the Application
Run the Flask app:
```bash
python app.py
```

By default, the application will run on `http://0.0.0.0:80`.
You can change this by going into app.py and changing the port on the last two lines of the file.

---

## Default Manager Credentials

- **Username**: `admin`
- **Password**: `PASSWORD`

Make sure to log in and change the manager's password immediately.
You can manage user accounts and change passwords at http://localhost:80/manage_users
You can choose not to use authentication by instead running the no auth version. (included in the same zip file)

---

## Usage Instructions

### Logging In
1. Navigate to `/login` in your browser.
2. Enter your username and password.

### Manager Role
- Add/Remove/Update user accounts.
- Add/Remove movies.
- View and manage RFID passes.
- End all active movie passes.

### Box Office Role
- Assign RFID tags to movies.
- Override existing tags if necessary.

### Pass Checker Role
- Verify RFID tags for the correct movie.
- End movie passes for a specific movie.

---

## Notes

1. The `auth.db` and `movie_theater.db` files are created in the project directory. Do not delete them unless resetting the databases.
2. The application uses hashed passwords for security. I suggest that you change the hash type in app.py. 
3. Styling for the login page is defined in `static/login.css`.
4. Use this on a private network so that ONLY staff may go to the site. It may be vulnerable to SQL injections.

---

## Troubleshooting

- **Error: `no such table: movies`**
  Ensure you have run `create-theater-db.py` to initialize the database.
  
- **Cannot Log In**:
  Check that the credentials are correct. Reset the database if necessary using the setup steps above. If you are still having issues, use the version without authentication. (also in the zip)

- **Styles Not Loading**:
  Ensure the `static` folder is present and contains the required CSS files.

---

  ## Issues
  You can contact me at me@ahmad-mahrous.com

---

#### By Ahmad Mahrous 2024
