# Django in Termux
This guide provides detailed steps for installing Django on Termux, a terminal emulator for Android.

## Table of Contents
- [Auto Install](#auto-install)
- [Manual Process](#manual-process)
  - Step 1: [Update Termux Package List](#update-termux-package-list)
  - Step 2: [Install Python and Git](#install-python-and-git)
  - Step 3: [Install Django and Required Packages](#install-django,-and-required-packages)
  - Step 4: [Verify Installation](#verify-installation)
  - Step 5: [Create a Django Project](#create-a-django-project)
  - Step 6: [Run the Development Server](#run-the-development-server)
- Question: [Why We Do Not Recommend Installing Django in a Virtual Environment](#why-we-do-not-recommend-installing-django-in-a-virtual-environment)
- [License](#license)
- [Uses](#uses)
- [Contributing](#contributing)

---

## Video Tutorial
For a visual guide on installing django in Termux, watch the YouTube video tutorial:
[![How to install django in termux without pullow and cryptography error](http://img.youtube.com/vi/LYsJdeZMnBI/0.jpg)](http://www.youtube.com/watch?v=LYsJdeZMnBI "How to install django in termux without pullow and cryptography error")

### Auto Install
To automatically install all required packages, execute the following command:
```bash
curl -s https://raw.githubusercontent.com/cyberkernelofficial/django-in-termux/main/commands.txt | bash
```

### Manual Process
#### Step 1: Update Termux Package List
Ensure your package list is up to date with the following command:
```bash
pkg update -y && pkg upgrade -y
```

#### Step 2: Install Python and Git
Install Python and Git using the package manager pkg:
```bash
pkg install python3 git -y
```

#### Step 3: Install Django and Required Packages
1. Install Django using pip, the Python package manager:
```bash
pip install django
```
2. For image processing in Django, install the python-pillow package:
```bash
pkg install python-pillow -y
```
3. To manage date and time effectively, Django requires tzdata:
```bash
pip install tzdata
```

#### Step 4: Verify Installation
Confirm the Django installation by checking its version:
```bash
django-admin --version
```

#### Step 5: Create a Django Project
Create a new Django project with the following command:
```bash
django-admin startproject mysite
```

#### Step 6: Run the Development Server
Move into your project directory:
```bash
cd mysite
```
Start the Django development server:
```bash
python manage.py runserver
```
Visit http://127.0.0.1:8000 in your web browser to view your Django project.

## Why We Do Not Recommend Installing Django in a Virtual Environment
When installing the Pillow package in Termux using pip, some devices encounter errors.
As a workaround, we suggest using the python-pillow package instead of directly installing from pip.
Furthermore, activating a virtual environment may cause Pillow to malfunction due to isolation from its necessary dependencies.
Hence, we recommend installing Django globally to ensure its seamless functionality.

---

## License
This project is licensed under the [MIT](LICENSE) License.
  
## Uses
Feel free to use this guide for installing Django on Termux interactively.

## Contributing
Contributions are welcome!
If you have any improvements or suggestions, please feel free to create a pull request.
