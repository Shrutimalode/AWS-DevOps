# 🖼️ AMI (Amazon Machine Image)

> **AMI (Amazon Machine Image)** is a template/blueprint that contains software configurations such as the **Operating System, applications, and application server**.

---

## 📦 Types of AMI

There are two different types of AMI:

1. **Default AMI** — These are the AMIs provided by third-party providers.
2. **Custom AMI** — An AMI created from an existing EC2 instance.

---

## 🚀 Using AMI

AMI can be used for:

### 1. 💾 Backup of an EC2 Instance

You can get the backup of an instance, including:

- 📁 Files
- 📂 Directories
- 🛠️ Applications
- ⚙️ Operating System

### 2. 📋 Creating a Template

You can create a template to **launch multiple instances at the same time** with the same configuration.

---

## 💾 Backup of an EC2 Instance

There are two ways to get the backup of your EC2 Instance:

1. **AMI (Amazon Machine Image)**
2. **Snapshots**

### Example

Suppose an EC2 instance contains:

**Applications / Tools**
- Maven
- Python
- Java
- Git

**Files**
- File1
- File2
- File3

**Directories**
- Dir1
- Dir2
- Dir3

When you create an **AMI**, the configuration of the instance is captured as a reusable image.

> ⚠️ **Note:** After creating the backup, if you create new resources in the instance, you need to take the backup again to include those changes.

---

## 🛠️ Steps to Create AMI

1. Select the instance that you want to create a backup of.
2. Click **Actions** → **Image and templates**.
3. Select **Create image**.
4. Give a **Name** and **Description**.
5. Click **Create**.

---

## 🚀 Steps to Create an Instance Using AMI

1. In the **AWS EC2 Dashboard**, search for **AMI** on the left side.
2. Select the AMI from which you want to launch a new instance.
3. Click **Launch Instance**.
4. Give a name to the instance.
5. Follow the normal EC2 instance creation steps, but select the **Custom AMI** that you created.
6. Click **Launch Instance**.

---

# 📸 Snapshot

A **Snapshot** is used to get the backup of the **volume/storage**.

> 💡 **AMI** → Backup of an EC2 instance  
> **Snapshot** → Backup of an EBS volume/storage

---

## 🔄 Steps to Create AMI Using Snapshot

1. In the **EC2 Dashboard**, select **Snapshot**.
2. Select the snapshot from which you want to create an AMI.
3. Click **Actions** → **Create image from Snapshot**.
4. The image will be created as an **AMI**.
5. Using the created AMI, **launch an instance**.

---

## 🔁 AMI Backup Flow

```text
EC2 Instance
     │
     │ Create AMI
     ▼
Custom AMI
     │
     │ Launch
     ▼
New EC2 Instance
