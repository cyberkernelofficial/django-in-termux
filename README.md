# Django in Termux
## Installing Django on Termux
This guide will walk you through the process of installing Django on Termux, a terminal emulator for Android.

### Step 1: Update Termux Package List
Run the following command to update the package list in Termux:
```bash
pkg update -y && pkg upgrade -y
```

### Step 2: Install Python and Git
Install Python and Git using the package manager pkg:
```bash
pkg install python3 git -y
```

### Step 3: Install Django and required packages
Install Django using pip, the Python package manager:
```bash
pip install django
```
For image processing django needs pillow
```bash
pkg install python-pillow -y
```
For date and time management, django needs tzdata
```bash
pip install tzdata
```

### Step 4: Verify Installation
Verify Django installation by checking the version:
```bash
django-admin --version
```

### Step 5: Create a Django Project
Create a new Django project using the following command:
```bash
django-admin startproject mysite
```

### Step 6: Run the Development Server
Navigate into your project directory:
```bash
cd mysite
```
Start the Django development server:
```bash
python manage.py runserver
```
Visit http://127.0.0.1:8000 in your web browser to see your Django project running.
