# Lesson 01: Introduction to Linux

## 1. Learning Objectives

* Learn what an Operating System (OS) is.

* Understand what Linux is and why it is crucial for DevOps.

* Learn about Linux distributions (distros) and Linux Architecture.

* Understand basic Linux terminology.

## 2. Introduction

ආයුබෝවන්! මම ඔබේ Senior DevOps Engineer සහ Personal Mentor. DevOps ඉංජිනේරුවෙකු වීමේ ඔබේ ගමනට සාදරයෙන් පිළිගන්නවා!

අපි මුලින්ම බලමු **Operating System (OS)** එකක් කියන්නේ මොකක්ද කියලා.

Operating System එකක් කියන්නේ කම්පියුටර් එකේ Hardware (CPU, RAM, Hard Disk) සහ Software අතර සම්බන්ධතාවය ගොඩනගන ප්‍රධාන මෘදුකාංගයයි (Core Software). උදාහරණ ලෙස Windows, macOS සහ Linux දැක්විය හැකියි.

**Linux** කියන්නේ Open-source (නොමිලේ ලබාගත හැකි සහ source code එක වෙනස් කළ හැකි) Operating System kernel එකක් මත පදනම් වූ OS එකක්. 1991 දී Linus Torvalds විසින් මෙය නිර්මාණය කරන ලදී.

## 3. Why This Is Important for DevOps

DevOps Engineering වලදී Linux කියන්නේ අත්‍යවශ්‍යම skill එකක්.

* ලෝකයේ ප්‍රධාන ප්‍රමාණයේ Cloud Infrastructure (AWS, Azure, GCP) සහ Web Servers වලින් 90% කට වඩා run වෙන්නේ Linux මතයි.

* Docker, Kubernetes, CI/CD pipelines (Jenkins, GitHub Actions), Terraform වැනි සියලුම ප්‍රධාන DevOps tools ක්‍රියාත්මක වන්නේ Linux පරිසරයන් තුළයි.

* Linux වල stability, security සහ automation පහසුව නිසා DevOps වල හදවත ලෙස Linux සැලකේ.

## 4. Core Concepts

### a) Linux Architecture

Linux OS එක කොටස් 4 කින් සමන්විත වේ:

1. **Hardware:** CPU, Memory (RAM), Disks.

2. **Kernel:** Linux වල හදවත. Hardware සහ Software අතර සන්නිවේදනය පාලනය කරයි.

3. **Shell:** පරිශීලකයා (User) ලබාදෙන commands Kernel එකට තේරුම් කර දෙන Command Interpreter එක (උදා: Bash).

4. **System Libraries & Utilities:** Applications run වීමට සහ OS එක පාලනය කිරීමට අවශ්‍ය මෘදුකාංග (GUI, Applications, CLI Tools).

```
+---------------------------------------------------+
|                  User Applications                |
+---------------------------------------------------+
|               Shell / CLI / Utilities             |
+---------------------------------------------------+
|                  System Libraries                 |
+---------------------------------------------------+
|                    Linux Kernel                   |
+---------------------------------------------------+
|                 Hardware (CPU, RAM, Disk)         |
+---------------------------------------------------+

```

### b) Linux Distributions (Distros)

Linux Kernel එක පදනම් කරගෙන විවිධ සංවිධාන විසින් සකස් කරන ලද OS සංස්කරණ 'Distros' ලෙස හැඳින්වේ.

* **Ubuntu / Debian:** Beginner-friendly, servers සහ cloud සඳහා බහුලව භාවිත වේ.

* **Red Hat Enterprise Linux (RHEL) / CentOS / Rocky Linux:** Enterprise Business ආයතන වල බහුලව භාවිත වේ.

* **Alpine Linux:** Docker containers සඳහා ඉතා කුඩා (lightweight) Linux distro එකකි.

## 5. Important Technical Terms

| English Term | Sinhala Explanation | 
| ----- | ----- | 
| **Kernel** | Operating System එකේ ප්‍රධාන කොටස. Hardware සහ Applications පාලනය කරයි. | 
| **Shell** | Command Line හරහා User සහ Kernel අතර සම්බන්ධය ගොඩනගන Program එක. | 
| **Terminal** | Commands type කිරීමට භාවිත කරන Text-based User Interface එක. | 
| **Open-source** | Source code එක ඕනෑම කෙනෙකුට නොමිලේ බැලීමට, වෙනස් කිරීමට සහ භාවිත කිරීමට හැකි වීම. | 
| **Distribution (Distro)** | Linux kernel එක සමඟ අමතර tools සහ software එකතු කර සාදන ලද OS පැකේජයක්. | 

## 6. Commands and Syntax

පළමු පාඩමේදී අපි Linux Terminal එකේ භාවිත වන මූලිකම Command එකක් බලමු:

**Command:**

```
uname -a

```

**Sinhala Explanation:**
`uname` කියන්නේ System Information පෙන්වන command එකයි. `-a` (all) කෑල්ල එකතු කළ විට system එකේ Kernel version එක, Operating System නම සහ Architecture (64-bit) එක සම්පූර්ණයෙන්ම පෙන්වයි.

## 7. Practical Examples

ඔබේ Linux Terminal එක Open කර පහත command එක run කර බලන්න:

```
uname -a

```

ලැබෙන Output එකෙන් ඔබේ Linux System එකේ Kernel details බලාගත හැක.

## 8. Hands-on Exercises

අද දින සඳහා ඔබේ පළමු practical exercise එක:

1. ඔබේ Linux පරිගණකයේ Terminal එක Open කරන්න.

2. `uname -a` command එක run කරන්න.

3. ඊළඟට `whoami` command එක run කර බලන්න (මෙයින් දැනට login වී සිටින User කවුදැයි පෙන්වයි).

## 9. Mini Project

ලිනක්ස් System එකේ විස්තර පරීක්ෂා කිරීම:

* Terminal එකේ `uname -r` (Kernel release) සහ `lsb_release -a` හෝ `cat /etc/os-release` (Linux Distribution details) සටහන් කරගන්න.

## 10. Common Errors and Troubleshooting

* **Error:** `command not found`

  * **Reason:** ඔබ Command එකේ අකුරක් වැරදියට type කර ඇත (Case-sensitive: Linux වල small/capital අකුරු වෙනස් වේ).

  * **Fix:** Command එකේ spelling නිවැරදිව type කරන්න.

## 11. Interview Questions

1. **What is Linux and why is it preferred for servers?**

   * *Explanation:* Linux is an open-source, highly secure, stable, and lightweight operating system, making it ideal for high-performance server environments.

2. **What is the difference between Linux Kernel and Linux OS?**

   * *Explanation:* Kernel is the core component managing hardware, while Linux OS includes the Kernel plus shell, system libraries, and GUI/applications.

3. **What is a Linux Distribution? Give examples.**

   * *Explanation:* A distribution is an operating system built from the Linux kernel and a collection of software. Examples: Ubuntu, RHEL, CentOS, Debian.

4. **What is a Shell in Linux?**

   * *Explanation:* A shell is a command-line interface program that interprets user commands and sends them to the kernel for execution.

5. **What command is used to check system information in Linux?**

   * *Explanation:* `uname -a` command displays detailed system information including kernel version and system architecture.

## 12. Knowledge Check

1. Linux Kernel එක සොයාගත්තේ කවුද?

2. Kernel එකේ ප්‍රධාන කාර්යය කුමක්ද?

3. Popular Linux distributions 3ක් නම් කරන්න.

4. Linux වල Command line interface එක හඳුන්වන නම කුමක්ද?

5. Login වී සිටින user පරික්ෂා කිරීමට ගන්නා command එක කුමක්ද?

## 13. Homework

1. ඔබේ Linux පරිගණකයේ Terminal එකක් open කරන්න.

2. `uname -a` සහ `whoami` command දෙක run කර ලැබෙන output එක මට එවන්න.

## 14. Lesson Summary

අද පාඩමෙන් අපි Operating System එකක් යනු කුමක්ද, Linux වල වැදගත්කම, Linux Architecture එක (Hardware, Kernel, Shell, Applications), Linux Distros සහ මූලිකම commands කීපයක් ගැන ඉගෙන ගත්තා.

## 15. Next Lesson

**Lesson 02: Linux Terminal and Basic Navigation Commands** (`pwd`, `ls`, `cd`, `mkdir`, `touch`, etc.)