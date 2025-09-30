# Day 1 – AWS Basics & IAM

## 🎯 Goal for the Day
Understand the core purpose of **AWS Identity and Access Management (IAM)** and set up secure access for hands-on AWS practice through the CLI.

---

## 🌐 What is IAM?
AWS **Identity and Access Management (IAM)** is a service that controls who can access your AWS account and what they can do.  
It covers two main ideas:
- **Authentication** → Who can sign in  
- **Authorization** → What actions they can perform  

### 🔑 Key Components
- **Users** → Individual identities (person or service)  
- **Groups** → Collections of users with shared permissions  
- **Roles** → Temporary identities assumed to access resources  
- **Policies** → JSON documents that define permissions  

**Best Practice:**  
- Never use the **root user** for daily work.  
- Create IAM users with **programmatic access (CLI/SDK)** and **console access**.  
- Apply the **least-privilege principle** (only the permissions needed).

## 🛠️ Steps-I-followed:

1. **Created IAM User**  
   - Went to **IAM → Users → Create user**  
   - Enabled **programmatic + console access**  
   - Attached `AdministratorAccess` policy (for practice)  
   - 📸 *Screenshot:*  
     ![IAM User Created](./screenshots/iam-user-created.png)

2. **Generated Access Keys**  
   - Downloaded `.csv` with **Access Key ID** and **Secret Access Key**  
   - These are used only for CLI/SDK access (not console login)  
   - 📸 *Screenshot:*  
     ![Access Key Generated](./screenshots/access-key-generated.png)

3. **Configured AWS CLI**  
   - Ran:
     ```bash
     aws configure
     ```  
   - Entered Access Key ID, Secret Access Key, region (`us-east-1`), and output (`json`)  
   - 📸 *Screenshot:*  
     ![CLI Configured](./screenshots/cli-configured.png)
