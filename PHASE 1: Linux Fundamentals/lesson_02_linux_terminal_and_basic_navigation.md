# Lesson 02: Linux Terminal and Basic Navigation Commands

## 1. Learning Objectives

* Understand how the Linux filesystem hierarchy works.
* Learn essential navigation and directory management commands (`pwd`, `ls`, `cd`, `mkdir`).
* Learn file creation and viewing commands (`touch`, `cat`).
* Understand absolute vs relative paths.

## 2. Introduction

පළමු පාඩමෙන් අපි Linux කියන්නේ මොකක්ද කියලා බැලුවා. අද අපි ඉගෙන ගන්නේ Linux Terminal එක ඇතුළේ කොහොමද වැඩ කරන්නේ, file සහ folders (directories) manage කරන්නේ කොහොමද කියලයි. 

Windows වල අපි folders open කරන්න Mouse එකෙන් double click කරනවා නේද? Linux servers වල GUI (Graphical User Interface) එකක් නැහැ (ගොඩක් වෙලාවට). අපි හැමදේම කරන්නේ Text Commands හරහා Terminal එකෙන්.

## 3. Why This Is Important for DevOps

DevOps ඉංජිනේරුවෙකුට Cloud Servers (AWS EC2 වැනි) සමඟ වැඩ කිරීමට සිදු වන්නේ Command Line (CLI) හරහා පමණි. Server එකක configuration files වෙනස් කිරීමට, logs බලන්න සහ applications deploy කිරීමට මෙම navigation commands අත්‍යවශ්‍ය වේ.

## 4. Core Concepts

### a) Linux Filesystem Hierarchy
Linux වල සියලුම files සහ directories පවතින්නේ එකම Root directory එකක් යටතේ (`/`). Windows වල වගේ `C:` හෝ `D:` drives වෙන වෙනම නැත. සියල්ල `/` (Root) එකෙන් පටන් ගනී.

### b) Absolute Path vs Relative Path
* **Absolute Path:** `/home/ubuntu/projects` වැනි Root (`/`) එකේ සිට සම්පූර්ණ පාර (path).
* **Relative Path:** දැනට අපි ඉන්න තැනේ සිට යන පාර (උදා: `cd documents`).

## 5. Important Technical Terms

| English Term | Sinhala Explanation |
| :--- | :--- |
| **Directory** | Windows වල අපි හඳුන්වන Folder එකට Linux වල කියන නම. |
| **Path** | File එකක් හෝ Directory එකක් පිහිටා ඇති ස්ථානය (Address එක). |
| **Root Directory** | Linux filesystem එකේ මුල්ම සහ ප්‍රධානම directory එක (`/`). |
| **CLI (Command Line Interface)** | Keyboard එකෙන් commands type කර computer එක පාලනය කරන ක්‍රමය. |

## 6. Commands and Syntax

මෙන්න අද අපි ප්‍රගුණ කළ යුතු වැදගත් Commands ටික:

1. **`pwd` (Print Working Directory)**
   * **Sinhala:** දැනට ඔබ සිටින Directory එකේ සම්පූර්ණ path එක පෙන්වයි.
   * **Syntax:** `pwd`

2. **`ls` (List)**
   * **Sinhala:** දැනට ඉන්න folder එකේ තියෙන files සහ directories ලැයිස්තුව පෙන්වයි.
   * **Syntax:** `ls` හෝ `ls -l` (detailed view), `ls -a` (hidden files ඇතුළුව).

3. **`cd` (Change Directory)**
   * **Sinhala:** වෙනත් folder එකකට මාරු වීමට (navigate වීමට) භාවිත කරයි.
   * **Syntax:** `cd <directory_name>` (ഉदा: `cd documents`)

4. **`mkdir` (Make Directory)**
   * **Sinhala:** අලුත් folder (directory) එකක් සෑදීමට.
   * **Syntax:** `mkdir <folder_name>`

5. **`touch`**
   * **Sinhala:** හිස් file එකක් සෑදීමට.
   * **Syntax:** `touch <file_name>`

6. **`cat` (Concatenate)**
   * **Sinhala:** file එකක අන්තර්ගතය (content) terminal එකේ පෙන්වීමට.
   * **Syntax:** `cat <file_name>`

## 7. Practical Examples

Terminal එකේ පහත commands පිළිවෙලින් run කර බලන්න:

```bash
pwd
ls
mkdir devops-lab
cd devops-lab
touch test.txt
ls
```

## 8. Hands-on Exercises

1. ඔබේ home directory එකේ සිට `linux-practice` නමින් අලුත් folder එකක් (directory) සෑදීමට `mkdir` command එක භාවිත කරන්න.
2. එම folder එක ඇතුළට ගොස් `notes.txt` නමින් file එකක් `touch` command එකෙන් සාදන්න.
3. `pwd` command එක භාවිතයෙන් ඔබ දැන් සිටින තැන තහවුරු කරගන්න.

## 9. Mini Project

* **Task:** `devops-project` නමින් folder එකක් සාදා, ඒ තුළ `config.json` සහ `script.sh` යන files දෙක නිර්මාණය කර `ls -l` මඟින් පරීක්ෂා කරන්න.

## 10. Common Errors and Troubleshooting

* **Error:** `No such file or directory`
  * **Reason:** ඔබ සඳහන් කළ නමින් folder එකක් හෝ file එකක් නැහැ, නැතහොත් නම වැරදියට type කර ඇත.
  * **Fix:** `ls` මඟින් නම නිවැරදිදැයි පරීක්ෂා කර නැවත උත්සාහ කරන්න.

## 11. Interview Questions

1. **What is the root directory in Linux?**
   * *Explanation:* The root directory is the topmost level of the Linux filesystem hierarchy, denoted by a forward slash (`/`).
2. **What is the difference between `ls` and `ls -l`?**
   * *Explanation:* `ls` lists files simply, while `ls -l` lists them in a long format including permissions, owner, size, and timestamp.
3. **How do you create a directory using the command line?**
   * *Explanation:* Using the `mkdir` command followed by the directory name (e.g., `mkdir my-folder`).
4. **What does `pwd` stand for and what does it do?**
   * *Explanation:* Print Working Directory; it prints the full path of the current working directory.
5. **How can you create an empty file quickly?**
   * *Explanation:* Using the `touch` command followed by the filename (e.g., `touch file.txt`).

## 12. Knowledge Check

1. දැනට ඉන්න folder එක පෙන්වන command එක කුමක්ද?
2. අලුتෙන් folder එකක් හදන්න පාවිච්චි කරන command එක මොකක්ද?
3. Linux වල සියලුම files පටන් ගන්නා ප්‍රධාන root directory එක ලියන්න.
4. හිස් file එකක් හදන්න පාවිච්චි කරන්නේ මොකක්ද?
5. `cd ..` command එකෙන් සිදුවන්නේ කුමක්ද?

## 13. Homework

1. `linux-practice` folder එක ඇතුළේ `day2.txt` නමින් file එකක් සාදා, එහි output එක මට එවන්න.
2. ඔබ `pwd` command එකෙන් ලබාගත් path එක මෙහි සටහන් කරන්න.

## 14. Lesson Summary

අද පාඩමෙන් අපි Linux filesystem structure එක, absolute/relative paths සහ `pwd`, `ls`, `cd`, `mkdir`, `touch` වැනි මූලික navigation commands භාවිතා කරන ආකාරය ඉගෙන ගත්තා.

## 15. Next Lesson

**Lesson 03: File and Directory Management** (`cp`, `mv`, `rm`, `cat`, `grep`, `find`)