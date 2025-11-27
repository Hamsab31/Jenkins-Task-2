# Jenkins CI/CD Pipeline with GitHub Webhook and Email Notification

This project demonstrates a simple CI/CD automation workflow using **Jenkins**, **GitHub**, and **AWS EC2**.  
When a new commit is pushed to GitHub, Jenkins automatically triggers a build, runs a shell script, and sends the output to the user via email.

---

## 🚀 Objective

- Create a script file and push it to GitHub  
- Configure Jenkins on AWS EC2  
- Connect Jenkins to GitHub via Webhook  
- Automatically trigger Jenkins build on every Git commit  
- Send build results through email  
- Upload screenshots of all steps to GitHub

---

## 🧱 Tech Stack Used

- **AWS EC2 (Ubuntu 22.04)** – Jenkins server  
- **GitHub** – Code repository  
- **Jenkins** – CI/CD automation  
- **Gmail SMTP** – Email notifications  

---

## 📌 Project Workflow

1. A `script.sh` file is pushed to the GitHub repository  
2. GitHub Webhook sends a notification to Jenkins  
3. Jenkins automatically pulls the latest code  
4. Jenkins executes the shell script  
5. Jenkins sends an email with the build result  
6. Build logs and screenshots are uploaded to GitHub  

---

## 📜 Script File (script.sh)

```bash
#!/bin/bash
echo "======================="
echo "Jenkins CI Demo Script"
echo "Build Time: $(date)"
echo "Branch: $GIT_BRANCH"
echo "Commit: $GIT_COMMIT"
echo "======================="
