# 🌐 How to Make a Website Using WordPress

---

# 📘 Introduction

---

# 🛠️ Step 1: Install Local Server (XAMPP)

Download and install **XAMPP** from Apache Friends.

* Visit the download page
* Choose your platform (**Windows / Linux / Mac**)
* Click **Download**

[Download XAMPP]()

---

# ▶️ Step 2: Run XAMPP

After installing XAMPP:

* Open the application
* Start the following services:

  * **Apache**
  * **MySQL**

This will activate your local web server. 

---

# ⚠️ Step 3: Fix Port Issues (If Needed)

If Apache does not start, port **80** may already be in use by another application.

### Solution:

* Click **Config** next to Apache
* Find:

```txt
Listen 80
```

* Change it to another value, for example:

```txt
Listen 1234
```

Then use `localhost:1234` in your browser. 

---

# 🌍 Step 4: Check Localhost

Open your browser and type:

```txt
localhost
```

Or if you changed the port:

```txt
localhost:1234
```

If it works, your local server is running correctly.

---

# 🗄️ Step 5: Open phpMyAdmin

phpMyAdmin is your MySQL database panel where WordPress stores:

* Posts
* Comments
* Username
* Password
* Website Data

Open:

```txt
localhost/phpmyadmin
```

---

# 📥 Step 6: Download WordPress
Download the latest version of WordPress from the official website.
Then:

* Copy the ZIP file into:

```txt
C:\xampp\htdocs
```

* Extract it
* A folder named **wordpress** will be created. 

---

# 🏗️ Step 7: Create Database

Inside phpMyAdmin:

* Click **New**
* Enter any database name

  * Example: `mywebsite`

---

# 🚀 Step 8: Run WordPress Installer

Open your browser:

```txt
http://localhost/wordpress/
```

You will see the WordPress setup page. Click:

**Let's go**

Fill in the following details:

| Field         | Value                 |
| ------------- | --------------------- |
| Database Name | Your created database |
| Username      | root                  |
| Password      | Leave empty           |
| Database Host | localhost             |
| Table Prefix  | wp_ (default)         |

Then click:

* Submit
* Run the Install

---

# 👤 Step 9: Website Setup

Now enter:

* Site Name
* Username
* Password
* Email Address

> The username and password are your **Admin Login Credentials**. Keep them secure.

Click:

**Install WordPress** 

---

# 🔐 Step 10: Login to Dashboard

After installation, login using your credentials.

Admin panel URL:

```txt
http://localhost/wordpress/wp-admin/
```

From here you can manage and customize your website. 

---

# 🏠 Step 11: View Homepage

Visit:

```txt
http://localhost/wordpress/index.php
```

You will see the default WordPress homepage.

---
