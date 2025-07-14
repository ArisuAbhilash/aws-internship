<p align="center">
  <img src="screenshots/ebs-logo.png" width="120"/>
</p>

<h1 align="center" style="color:#2E86C1;">AWS EBS – Elastic Block Storage Overview</h1>
</br>

<h3 align="left" style="color:#2E86C1;">📝 Introduction</h3>

---

**EBS (Elastic Block Store)** is a **virtual storage service** in AWS that provides persistent block-level storage for EC2 instances.

Think of EC2 as the **virtual server** and EBS as the **virtual hard drive** attached to it.

---

<h3 align="left" style="color:#2E86C1;">📦 What is EBS?</h3>

---

- **EBS = Elastic Block Storage**  
- Used for **storing data, OS files, and applications**.
- **Zonal service** → EBS volumes are tied to a specific **Availability Zone**.

---

<h3 align="left" style="color:#2E86C1;">🧰 Key Features</h3>

---

- **Persistent Storage:**  
  Data is preserved even when the EC2 instance is stopped (unless deleted on termination).

- **Volume Size:**  
  - Once declared, **EBS size cannot be reduced**.  
  - **You can increase the size** at any time.

- **IOPS (Input/Output Operations Per Second):**  
  Measures the speed of reading/writing data on your volume.

---

<h3 align="left" style="color:#2E86C1;">💾 Volume Types</h3>

---

| Type | Backed By | Use Case |
|------|-----------|----------|
| **SSD-backed Volumes** | Solid State Drives | High-performance workloads, frequent read/write |
| **HDD-backed Volumes** | Hard Disk Drives | Big data, throughput-intensive workloads |

---

<h3 align="left" style="color:#2E86C1;">🗃️ Types of EBS Volumes in EC2</h3>

---

1. **Root Volume**  
   - Contains the **Operating System (OS)** and **boot files**  
   - Typically **deleted automatically** when the instance is terminated (unless configured otherwise)

2. **Additional Volume (Data Volume)**  
   - Used for **storing data, applications, or backups**  
   - **Does not get deleted automatically** unless you manually delete it.

---

<h3 align="left" style="color:#2E86C1;">🗑️ Deletion Behavior</h3>

---

- When you **terminate an EC2 instance**:
  - **Root Volume** → Usually **deleted automatically**  
  - **Additional Volumes** → **Remain available** unless you manually delete them.

---



## 🔗 Resources

- [AWS EBS Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)
- [AWS Free Tier](https://aws.amazon.com/free)

