# ⚙️ WordPress Installation — Complete Step-by-Step Guide

> This guide walks you through everything you need to install WordPress locally or on a web server — from system requirements to your very first login.

---

## 📋 Table of Contents

- [System Requirements](#-system-requirements)
- [Download WordPress](#-download-wordpress)
- [Installation Steps](#-installation-steps)
  - [Step 1 — Choose Your Language](#step-1--choose-your-language)
  - [Step 2 — Pre-Installation Info](#step-2--pre-installation-info)
  - [Step 3 — Database Credentials](#step-3--database-credentials)
  - [Step 4 — Run the Install](#step-4--run-the-install)
  - [Step 5 — Site Admin Info](#step-5--site-admin-info)
  - [Step 6 — Log In](#step-6--log-in)

---

## 🖥️ System Requirements

Before installing WordPress, you need a local server environment. Choose the stack that matches your operating system:

| Operating System | Required Stack | Components |
|---|---|---|
| 🪟 **Windows** | WAMP | Windows + Apache + MySQL + PHP |
| 🐧 **Linux** | LAMP | Linux + Apache + MySQL + PHP |
| 🍎 **macOS** | MAMP | Macintosh + Apache + MySQL + PHP |
| 🌐 **Cross-platform** | XAMPP | Apache + MariaDB + PHP + Perl |

> 💡 **Compatibility:** WordPress requires **PHP 5.2+** and **MySQL 5.0+**

---

## 📥 Download WordPress

WordPress is a **free and open-source** platform, distributed under the **GNU General Public License (GPL)**. You can download it directly from the official website:

🔗 **[https://wordpress.org/download/](https://wordpress.org/download/)**

![WordPress Download Page](images/step-download.png)

> The latest stable release is available in two formats: `.zip` and `.tar.gz`. Download either and extract it to your local server's project folder.

---

## 🚀 Installation Steps

### Before You Begin

1. Download WordPress and upload/extract it into your **localhost** or **web server project folder**
2. Open your browser and navigate to your WordPress folder URL:
   ```
   http://localhost/your_wordpress_folder_name
   ```
3. Create an **empty MySQL database** — the installer will need it

---

### Step 1 — Choose Your Language

The WordPress Setup Wizard launches automatically. The first screen asks you to select your preferred language.

![Step 1 — Language Selection](images/step1-language.png)

Choose your language from the dropdown list and click **Continue** to proceed.

---

### Step 2 — Pre-Installation Info

The second screen displays a brief overview of the information you'll need before proceeding with the installation — primarily your **database credentials**.

> 📝 Make sure you have your MySQL database name, username, and password ready before moving to the next step.

---

### Step 3 — Database Credentials

This is where you connect WordPress to your MySQL database. Fill in the following fields:

![Step 3 — Database Connection Form](images/step3-database.png)

| Field | Description | Default |
|---|---|---|
| **Database Name** | The name of the MySQL database you created | `wordpress` |
| **Username** | Your MySQL database username | `root` |
| **Password** | Your MySQL database password | _(your password)_ |
| **Database Host** | The hostname of your database server | `localhost` |
| **Table Prefix** | Prefix for database tables — change this to run multiple sites on one database | `wp_` |

Once all fields are filled in, click the **Submit** button.

---

### Step 4 — Run the Install

WordPress verifies your database credentials and confirms the connection was successful.

![Step 4 — Run the Install](images/step4-run-install.png)

If everything is correct, you'll see a success message. Click the **"Run the Install"** button to continue.

---

### Step 5 — Site Admin Information

This is the final configuration step. Provide the following details for your WordPress site:

![Step 5 — Site Admin Info](images/step5-site-info.png)

| Field | Description |
|---|---|
| **Site Title** | The name of your WordPress website |
| **Username** | Your admin login username |
| **Password** | A strong password for your admin account |
| **Your Email** | Admin email address for notifications |
| **Search Engine Visibility** | Check to discourage search engines from indexing (useful during development) |

> ⚠️ **Important:** Store your password in a safe place — you'll need it every time you log in!

Once the form is complete, click **"Install WordPress"**.

---

### Step 6 — Log In

The installation is complete! You'll be redirected to the **WordPress Admin Login screen**.

![Step 6 — WordPress Login Screen](images/step6-login.png)

Enter the **username** and **password** you set in the previous step and click **Log In**.

---

## 🎉 You're All Set!

Congratulations — WordPress is now successfully installed and ready to use. You'll land on the WordPress **Admin Dashboard**, where you can start building and customizing your site.

---

## 📁 File Structure Reference

```
your_wordpress_folder/
├── wp-admin/          # Admin panel files
├── wp-content/        # Themes, plugins, uploads
├── wp-includes/       # Core WordPress files
├── wp-config.php      # Database configuration (auto-generated)
└── index.php          # Entry point
```

---

*Happy building with WordPress! 🚀*
