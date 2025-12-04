<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

<p align="center">
  <img alt="Typing" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=700&color=FFC72C&center=true&vCenter=true&width=650&lines=Designed+for+Everyone%2C+Built+for+the+Future;Where+Beginners+Start+and+Developers+Grow;A+Simple+Language+for+Big+Ideas;Write+Less%2C+Create+More+%E2%80%94+With+NISR+PL;Powerful+for+Experts%2C+Friendly+for+Beginners;Code+in+Your+Language+%E2%80%94+NISR+Speaks+Many;Multilingual+Language+for+Global+Developers;Learning+to+Code+Has+Never+Been+This+Simple;From+Zero+to+Pro+%E2%80%94+The+NISR+Way;Teach%2C+Learn%2C+Build+%E2%80%94+All+with+NISR+PL" />
</p>


<p align="center">
  <a href="https://Github.com/Nisr-programming-language/Nisr_PL">
    <img src="https://img.shields.io/badge/Try%20NISR-Online-green?style=for-the-badge" />
  </a>
</p>

---




# How to Set Up Nisr

## 1. Install Nisr
- Install Nisr.exe on your system.
- Go to the installation folder.
- Add this folder to your system PATH.

## 2. Verify Installation
- Open Command Prompt and run:


> nsrc --version
> nsri --version


## 3. Compile and Run Your First Program
- Create a new folder anywhere.
- Create a file named main.ns and write:

> print("Hello World")

- Open CMD in that folder and compile: nsrc main.ns
- This will create main.nb
- Run it using: nsri main.nb
## 4. Setting Up Your Own Language
**Nisr** allows you to create a custom programming language with translated keywords.

## 4.1 Prepare Setup Tool
- Go to the Nisr installation folder → tools folder.
- Add this folder to your system PATH.
- Verify installation:
> setup --version
## 4.2 Check Available Languages
- Run:
> setup --list-langs
## 4.3 Extract a Sample Configuration
- Choose a language code (example: **en**)
- Run:
> setup -ex-l en
- This will extract all the configurations to the folder called nisr_config
## 4.4 Edit Language Configuration
- Each file contains key-value pairs: **Key = Nisr keyword, Value = your translation**
- **Do NOT delete or add keys**, only edit values.
## 4.5 Create Your Custom Language
- Run:
> setup -cl nisr_config custom_code
- custom_code is the new language code you choose.
- Follow the instructions shown in CMD.
## 4.6 Compile Using Your Custom Language
- Compile your program with:
> nsrc main.ns --lang=custom_code
- Run it:
> nsri main.nb
## Setup Complete
You have successfully:

- Installed Nisr
- Compiled and ran your first program
- Set up a custom programming language
- Compiled and ran programs using your custom language
> **Note**: Keep your **nisr_config** folder safe. Editing keys incorrectly may cause errors.













---

### 📘 Learn more:
- [Getting Started](01-Getting%20Started.md)
- [Basic Syntax](02-Basic%20Syntax.md)
- [Expressions and Operators](03-Expressions%20and%20Operators.md)
- [List, Tuple and Dictionary](04-List,%20Tuple%20and%20Dictionary.md)
- [String Manipulation](05-String%20Manipulation.md)
- [Control Flow and Error Handling](06-Control%20Flow%20and%20Error%20Handling.md)
- [Built-in-Functions](07-Built-in-Functions.md)
- [Functions](08-Functions.md)
- [Libraries and Modules](09-Libraries%20and%20Modules.md)
- [Object Oriented Programming](10-Object%20Oriented%20Programming.md)
- [Language Configuration](11-Language%20Configuration.md)


---

<p align="center">
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💬 Give Feedback-blue?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/🐞 Report Bug-red?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💡 Suggestions-yellow?style=for-the-badge" />
  </a>
  <a href="mailto:nisrprogramminglanguage@gmail.com">
    <img src="https://img.shields.io/badge/✉️ Email Us-green?style=for-the-badge" />
  </a>
  <a href="https://t.me/Nisr_PL">
    <img src="https://img.shields.io/badge/📱 Telegram-blue?style=for-the-badge" />
  </a>
</p>

---
