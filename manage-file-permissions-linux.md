# 🔐 Manage File Permissions in Linux

## 📋 Project Description

As a security professional working with a research team, I was responsible for checking and updating file permissions on a Linux system. The goal was to make sure only authorized users had the correct level of access and to enforce the **principle of least privilege**.

---

## 🛠️ Steps

### 1. Check Current Permissions

I used the following command to view all files (including hidden files) and their current permissions:

```bash
ls -la
```

### 2. Remove Write Permission for Others

I removed write access for "others" on the file `project_k.txt` so that only the owner and group could modify it:

```bash
chmod o-w project_k.txt
```

### 3. Secure a Hidden File

I updated the permissions on the hidden file `.project_x.txt` by removing write access for the user and group, while still allowing the group to read the file:

```bash
chmod u-w,g-w,g+r .project_x.txt
```

### 4. Restrict Directory Access

I removed execute permission from the group on the `drafts` directory so that unauthorized users could not enter it:

```bash
chmod g-x drafts
```

---

## ✅ Summary

In this activity, I practiced using `ls -la` to inspect file and directory permissions and `chmod` to change them. These skills are important for securing sensitive files and directories on Linux systems and following the **principle of least privilege**.

---

## 🧠 Skills Demonstrated

- Linux file permission auditing
- `chmod` symbolic mode (user/group/other access control)
- Hidden file security
- Directory access restriction
- Principle of least privilege enforcement
