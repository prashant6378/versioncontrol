# 🔧 Mastering Version Control: A Deep Dive into SVN & Mercurial

## 📚 Introduction to Version Control Systems
Version Control Systems (**VCS**) are essential for managing software changes, enabling collaboration, and maintaining project history.

### ✨ Types of Version Control Systems
1. **Centralized Version Control Systems (CVCS)** – A single central server stores all versions (e.g., **Subversion (SVN)**).
2. **Distributed Version Control Systems (DVCS)** – Each user has a full repository copy (e.g., **Mercurial (HG)**).

### 🌟 Why Use Version Control?
- ✅ Tracks all changes and keeps a history
- ✅ Supports collaboration among multiple developers
- ✅ Enables rollback to previous versions
- ✅ Facilitates branching, merging, and testing new features

---

## 🛠 Subversion (SVN)

SVN (**Apache Subversion**) is a **centralized version control system (CVCS)** that helps developers track changes to files and collaborate on projects efficiently.

## **🔹 Key Features of SVN**

1. **Centralized Repository**
   - A single server stores all files and version history.
   - Developers must connect to the server to commit or retrieve changes.

2. **Revision-Based Tracking**
   - Every commit creates a **new revision number** (e.g., `r1, r2, r3`).
   - Enables rolling back to previous versions.

3. **Atomic Commits**
   - Ensures all changes are committed together or not at all.

4. **Branching & Tagging**
   - SVN supports **directory-based branching and tagging**.

5. **Access Control & Permissions**
   - Allows restricting access to files and directories.

6. **Locking Mechanism (Exclusive Checkout)**
   - Prevents multiple users from modifying the same file simultaneously.

---

## **🔹 How SVN Works?**

### **1️⃣ Central Repository**
SVN uses a **single central repository** to store all files and history.

### **2️⃣ Working Copy**
Developers get a **local copy** of the repository to make changes.

### **3️⃣ Changes and Commits**
- Developers **edit files locally**.
- They **commit changes** to the repository.
- SVN assigns a **new revision number** for each commit.

### **4️⃣ Updates & Merging**
- Users **update** their working copy to get the latest changes.
- SVN helps **merge** modifications from different developers.

---

## **🔹 Basic SVN Commands**

| **Command** | **Description** |
|------------|----------------|
| `svn checkout <repo-url>` | Get a working copy of the repository |
| `svn update` | Update local copy with latest changes |
| `svn add <file>` | Add a new file to version control |
| `svn commit -m "Message"` | Commit changes to the repository |
| `svn revert <file>` | Undo local changes before committing |
| `svn status` | Show modified files |
| `svn log` | View commit history |
| `svn diff` | Compare changes between revisions |
| `svn resolve` | Resolve merge conflicts |

---

### 🔄 SVN Workflow
🔽 Checkout ➡️ 📝 Edit ➡️ ✨ Commit ➡️ ⬇️ Update ➡️ ⚔️ Resolve Conflicts

### 💡 Installing & Setting Up SVN on Windows
1. 💾 **Download & Install SVN** ([TortoiseSVN](https://tortoisesvn.net/)).
2. 🔄 Restart your system.
3. 📃 Verify installation:
   ```sh
   svn --version
   ```
   ![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20142716.png)


### ⚡ Essential SVN Commands
#### **📘 Step 1: Creating & Initializing a Repository**
```sh
svnadmin create C:\svn_repos\my_repo
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20143202.png)


#### **📂 Step 2: Checking Out a Repository**
```sh
svn checkout file:///C:/svn_repos/my_repo C:\Users\YourUser\my_working_copy
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021105.png)


#### **🔍 Step 3: Making Changes & Committing**
```sh
svn add C:\Users\YourUser\project\file.txt
svn commit -m "Added file.txt"
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021314.png)

#### **🔄 Step 4: Updating & Viewing Logs**
```sh
svn update  
svn log
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021435.png)

#### **↩️ Step 5: Reverting Changes**
```sh
svn revert file.txt
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021527.png)

#### **🎨 Step 6: Branching & Merging**
```sh
svn copy file:///C:/svn_repos/my_repo/trunk file:///C:/svn_repos/my_repo/branches/feature-branch -m "Creating a feature branch"
svn merge file:///C:/svn_repos/my_repo/branches/feature-branch
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021922.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20021949.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20022006.png)

---

## 🌐 Mercurial (HG)

Mercurial (**Hg**) is a **distributed version control system (DVCS)** designed for speed, efficiency, and ease of use. It enables developers to track changes in source code and collaborate effectively.

---

## **🔹 Key Features of Mercurial**

1. **Distributed Architecture**
   - Every developer has a complete copy of the repository.
   - No central server is required, but one can be used for collaboration.

2. **Fast Performance**
   - Optimized for handling large codebases efficiently.

3. **Simple and Intuitive Commands**
   - Commands are user-friendly and similar to Git.

4. **Atomic Commits**
   - Ensures that commits are completed successfully or not at all.

5. **Branching & Merging**
   - Supports easy branching and merging, preserving history.

6. **Scalability**
   - Handles projects of all sizes, from small teams to enterprise applications.

---

## **🔹 How Mercurial Works?**

### **1️⃣ Distributed Repositories**
Each user has a complete copy of the repository, enabling offline work.

### **2️⃣ Committing Changes**
- Developers **edit files locally**.
- They **commit changes**, creating a new revision in their local repository.

### **3️⃣ Pull & Push**
- Developers **pull** changes from others.
- They **push** their changes to a shared repository when ready.

### **4️⃣ Merging & Conflict Resolution**
- Mercurial provides tools to merge changes from multiple sources.

---

## **🔹 Basic Mercurial Commands**

| **Command** | **Description** |
|------------|----------------|
| `hg init` | Initialize a new Mercurial repository |
| `hg clone <repo-url>` | Clone an existing repository |
| `hg status` | Show modified files |
| `hg add <file>` | Add a new file to version control |
| `hg commit -m "Message"` | Commit changes to the repository |
| `hg pull` | Fetch changes from a remote repository |
| `hg push` | Push committed changes to a remote repository |
| `hg update` | Update working directory to a specific revision |
| `hg merge` | Merge branches |
| `hg log` | View commit history |

---

### 🔄 Mercurial Workflow
🔽 Clone ➡️ 📝 Edit ➡️ ✨ Commit ➡️ ⬆️ Push ➡️ ⬇️ Pull & Merge

### 💡 Installing & Setting Up Mercurial on Windows
1. 💾 **Download & Install Mercurial** ([TortoiseHg](https://tortoisehg.bitbucket.io/)).
2. 🔄 Restart your system.
3. 📃 Verify installation:
   ```sh
   hg --version
   ```
   ![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20023939.png)

### ⚡ Essential Mercurial Commands
#### **📘 Step 1: Creating & Initializing a Repository**
```sh
hg init my-hg-repo
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024030.png)

#### **📂 Step 2: Adding & Committing Files**
```sh
hg add newfile.txt  
hg commit -m "Added newfile.txt"
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024209.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024425.png)

#### **🔍 Step 3: Cloning, Updating & Reverting**
```sh
hg clone https://example.com/repo  
hg pull  
hg update  
hg log
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20024954.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025414.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025439.png)

#### **🎨 Step 4: Branching & Merging**
```sh
hg branch new-feature  
hg merge
```
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025807.png)
![Screenshot](https://raw.githubusercontent.com/TarakKatoch/DevOps-Class-Assignment/main/images/Screenshot%202025-02-14%20025834.png)

---

## 🏆 SVN vs. Mercurial: A Quick Comparison

| Feature       | Subversion (SVN) | Mercurial (HG) |
|--------------|----------------|----------------|
| Type        | Centralized VCS | Distributed VCS |
| Offline Work | ❌ Limited     | ✅ Fully Offline |
| Branching    | ⚠️ Complicated  | ✅ Simple & Fast |
| Performance  | 🐢 Slower       | 🚀 Faster |
| Learning Curve | 👍 Easier for Teams | 👍 Easier for Individuals |

---

## 🔧 Best Practices & Troubleshooting
- ✅ Use **SVN** for centralized team collaboration.
- ✅ Use **Mercurial** for offline flexibility.
- ✅ Write meaningful **commit messages**.
- ✅ Regularly **backup repositories**.
- ✅ Resolve **merge conflicts carefully**.

---

✨ *By: Tarak Katoch*  
 
