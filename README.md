<div align="center">

# 🔐 SSH Authentication Monitoring Dashboard (Splunk)

### 🚀 Real-Time SSH Security Monitoring • Brute-Force Detection • Geo-Attack Visualization

<p align="center">
  <img src="https://img.shields.io/badge/Splunk-Dashboard-black?style=for-the-badge&logo=splunk&logoColor=white" />
  <img src="https://img.shields.io/badge/Cybersecurity-Project-red?style=for-the-badge&logo=hackthebox&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-Logs-yellow?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge&logo=checkmarx&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/your-username/your-repo?style=social" />
  <img src="https://img.shields.io/github/forks/your-username/your-repo?style=social" />
  <img src="https://img.shields.io/github/watchers/your-username/your-repo?style=social" />
</p>

<img width="597" height="597" alt="image" src="https://github.com/user-attachments/assets/0d5b5a27-8194-440d-90e4-a66421a5eb5a" />

</div>

## 📌 Objective

The objective of this project is to design and implement a **Splunk dashboard** for monitoring **SSH authentication activity** on Linux servers.
The dashboard helps security analysts:

* Monitor total SSH activity
* Track successful and failed login attempts
* Detect brute-force attacks
* Visualize attack origins using geo-location data

This dashboard is designed with **consistent time filtering** and **security-focused visualizations** for effective threat detection.

---

## 🧪 Lab Setup

### Prerequisites

* Splunk Enterprise / Splunk Free
* SSH log data ingested in JSON format
* Indexed SSH log files:

  * `ssh_logs.json`
  * `ssh_logs_new.json`
* Linux servers:

  * `LinuxServer`
  * `LinuxNew`
<img width="1919" height="962" alt="1" src="https://github.com/user-attachments/assets/be1f9c0b-66a1-4c0d-8334-a4d35c0335ba" />
<img width="1919" height="968" alt="2" src="https://github.com/user-attachments/assets/eca5af37-616f-4374-bd5b-6d16ae1581b5" />
<img width="1919" height="965" alt="3" src="https://github.com/user-attachments/assets/34d79548-a661-4752-a327-7162183c11f3" />
<img width="1919" height="965" alt="4" src="https://github.com/user-attachments/assets/5d117cfc-faef-40d6-92d0-c810c53b929c" />
<img width="1919" height="966" alt="5" src="https://github.com/user-attachments/assets/39ac66e3-822a-4629-b3c4-600ece4b0295" />
<img width="1919" height="1079" alt="6" src="https://github.com/user-attachments/assets/04cad694-0439-43be-9f3f-28638da71a34" />
<img width="1919" height="966" alt="7" src="https://github.com/user-attachments/assets/43c19480-51a7-4e7a-952c-37680bfaf345" />
<img width="1919" height="965" alt="8" src="https://github.com/user-attachments/assets/0b8abe86-c689-436f-8e49-4fd0c4138d07" />
<img width="1919" height="964" alt="9" src="https://github.com/user-attachments/assets/a71f4587-9a24-4663-8a90-f549bdc21a62" />
<img width="1919" height="966" alt="10" src="https://github.com/user-attachments/assets/d672f528-5b69-419e-849c-9455ef2fc9e1" />
<img width="1919" height="966" alt="11" src="https://github.com/user-attachments/assets/3e004973-b950-4afa-a443-d524fce62f1e" />
<img width="1919" height="965" alt="12" src="https://github.com/user-attachments/assets/a2c4c934-2898-4ccd-9cf5-677f727af693" />
<img width="1919" height="967" alt="13" src="https://github.com/user-attachments/assets/a6d1271e-964b-4872-8560-782a96dbdc92" />
<img width="1919" height="967" alt="14" src="https://github.com/user-attachments/assets/591474a6-b933-495b-ae4d-a635055bf143" />
<img width="1919" height="964" alt="15" src="https://github.com/user-attachments/assets/4a5d9974-760f-486b-a81f-df10dd642806" />
<img width="1919" height="966" alt="16" src="https://github.com/user-attachments/assets/6607da3d-f3c2-49f0-9071-1027a7105eb4" />

---

## ⏱️ Task 0: Setting Up Time Range

### Goal

Ensure **consistent time filtering** across all dashboard panels.

### Steps

1. Click **Add Time Range Button**
2. Click **Add Input**
3. Select **Time**
4. Click the **Pencil Icon**
5. Set:

   * **Label:** `Time Range`
   * **Token:** `time_range`
6. Click **Add Input**
7. Select **Submit**

> ⚠️ **Note:**
> For **all future panels**, set the **Time Picker** to `time_range` for consistency.
<img width="1919" height="963" alt="17" src="https://github.com/user-attachments/assets/f15f0503-1a0a-4c1f-9fce-41596ebcb365" />
<img width="1919" height="965" alt="18" src="https://github.com/user-attachments/assets/8a1d07fd-0758-46f8-8a88-3e9bb12a41b2" />
<img width="1919" height="967" alt="19" src="https://github.com/user-attachments/assets/5b2140c7-018e-4bc6-8e4f-976199cefcc7" />
<img width="1919" height="968" alt="20" src="https://github.com/user-attachments/assets/6b7129e3-686e-4f1a-8857-f4d2e27fa252" />
<img width="1919" height="966" alt="21" src="https://github.com/user-attachments/assets/defff74c-e63f-4b50-a6b6-7446125eded7" />
<img width="1919" height="960" alt="22" src="https://github.com/user-attachments/assets/abe2e388-d3f0-4eff-968c-91dcc9b5c9b4" />
<img width="1919" height="965" alt="23" src="https://github.com/user-attachments/assets/9c70ffde-6c0f-420c-b68e-ad134c8d5361" />
<img width="1919" height="967" alt="24" src="https://github.com/user-attachments/assets/0fb7d072-7716-4480-a324-c5e52ef318e7" />
<img width="1919" height="967" alt="25" src="https://github.com/user-attachments/assets/00534714-ecb1-4e6e-8b6a-9e0dd7f8c433" />
<img width="1919" height="968" alt="26" src="https://github.com/user-attachments/assets/63eac551-0429-4f77-9ba5-f60749ae04bd" />

---

## 🔐 Task 1: Authentication Overview Panels

### Goal

Provide a **quick overview** of SSH authentication activity.

---

### 1️⃣ Total SSH Events

* **Panel Type:** Single Value
* **Time Picker:** `time_range`
* **Title:** `Total SSH Events`

**Search Query:**

```spl
source="ssh_logs.json" host="LinuxServer" sourcetype="_json"
| stats count AS "Total SSH Events"
```
<img width="1919" height="969" alt="28" src="https://github.com/user-attachments/assets/08a47363-1d74-4ccc-854d-522fe3f09d80" />
<img width="1919" height="966" alt="29" src="https://github.com/user-attachments/assets/5ae360c6-3352-4da1-938a-82ec4ce49c7a" />
<img width="1919" height="969" alt="30" src="https://github.com/user-attachments/assets/8de707f5-9c8e-4c99-88d2-c94e76d71a6c" />
<img width="1919" height="965" alt="31" src="https://github.com/user-attachments/assets/400a0bf3-7815-4755-987c-4faef2e9c2de" />
<img width="1919" height="966" alt="32" src="https://github.com/user-attachments/assets/ee587e94-8a7e-47b2-bc8a-3e0c30975df7" />
<img width="1919" height="966" alt="33" src="https://github.com/user-attachments/assets/a7aa3885-cec3-4a91-9ef5-bc6729fd4fe0" />
<img width="1919" height="964" alt="34" src="https://github.com/user-attachments/assets/8bc2e87f-aca8-4807-ad70-c58cd7cea186" />

---

### 2️⃣ Successful Logins

* **Panel Type:** Single Value
* **Time Picker:** `time_range`
* **Title:** `Successful Logins`

**Search Query:**

```spl
source="ssh_logs.json" host="LinuxServer" sourcetype="_json" event_type="Successful SSH Login"
| stats count AS "Successful Logins"
```
<img width="1919" height="964" alt="35" src="https://github.com/user-attachments/assets/e9eff64e-3e36-4fc1-9479-4eca34d9260c" />
<img width="1919" height="965" alt="36" src="https://github.com/user-attachments/assets/9d32b676-2866-41e8-99ab-d4d45e7ee407" />
<img width="1919" height="966" alt="37" src="https://github.com/user-attachments/assets/ae102203-b18e-4215-9113-375c193f31b0" />
<img width="1919" height="967" alt="38" src="https://github.com/user-attachments/assets/39d89ba0-7381-42c5-98ea-7f2468844da4" />
<img width="1919" height="967" alt="39" src="https://github.com/user-attachments/assets/5533393f-c393-493e-9b74-ca19296a9304" />
<img width="1919" height="966" alt="40" src="https://github.com/user-attachments/assets/bef298a3-eed7-4159-8278-6f177d3ce22e" />
<img width="1919" height="963" alt="41" src="https://github.com/user-attachments/assets/3b892a0c-c0c2-4a87-825f-b1f350240f48" />

---

### 3️⃣ Failed Logins

* **Panel Type:** Single Value
* **Time Picker:** `time_range`
* **Title:** `Failed Logins`

**Search Query:**

```spl
source="ssh_logs.json" host="LinuxServer" sourcetype="_json" event_type="Failed SSH Login"
| stats count AS "Failed Login"
```
<img width="1919" height="966" alt="42" src="https://github.com/user-attachments/assets/71b51232-3b3c-4929-8e1d-e8a1582c65f3" />
<img width="1919" height="966" alt="43" src="https://github.com/user-attachments/assets/32952263-9803-41d2-9d39-ad6c96f43059" />
<img width="1919" height="966" alt="44" src="https://github.com/user-attachments/assets/ebabbad1-6fb5-4f07-80cb-722fb9f6662d" />
<img width="1919" height="964" alt="45" src="https://github.com/user-attachments/assets/ad35e50c-3b51-4a0c-bc9e-1a674a4574ec" />
<img width="1919" height="966" alt="46" src="https://github.com/user-attachments/assets/3ea38856-072b-4a98-b65b-19b606064ace" />
<img width="1919" height="963" alt="47" src="https://github.com/user-attachments/assets/f49f3f1b-834b-4e8d-81af-399e8afcbd73" />
<img width="1919" height="967" alt="48" src="https://github.com/user-attachments/assets/df0eaf1c-103d-4ac4-b933-985966c7211f" />

---

### 4️⃣ Connection Without Authentication (Invalid Users)

* **Panel Type:** Single Value
* **Time Picker:** `time_range`
* **Title:** `Invalid User Attempts`

**Search Query:**

```spl
index=auth "sshd" "invalid user"
| stats count AS "Invalid User Attempts"
```
<img width="1919" height="964" alt="49" src="https://github.com/user-attachments/assets/28820985-d6ab-4109-98b9-8313d54381fc" />
<img width="1919" height="966" alt="50" src="https://github.com/user-attachments/assets/771b01c9-4c9e-4542-ae31-efd816f3ba6b" />
<img width="1919" height="966" alt="51" src="https://github.com/user-attachments/assets/c49d593e-5f4c-44db-adf3-dd616184a5d2" />
<img width="1919" height="967" alt="52" src="https://github.com/user-attachments/assets/f663d0d5-a7bc-4b3c-935d-610e13a6e160" />
<img width="1919" height="968" alt="53" src="https://github.com/user-attachments/assets/3410c49c-4259-4bf6-9646-02e0e51e8f54" />
<img width="1919" height="967" alt="54" src="https://github.com/user-attachments/assets/5aa3714b-b8ca-45a4-a4ae-ae42d671cac7" />
<img width="1919" height="971" alt="56" src="https://github.com/user-attachments/assets/ae623d18-7684-44ab-9e01-9020c5dd36ea" />

---

## 📈 Task 2: Login Activity Trends

### Goal

Analyze login patterns over time and **detect anomalies or attack behavior**.

---

### 1️⃣ Failed Logins by Username

* **Panel Type:** Bar Chart
* **Time Picker:** `time_range`
* **Title:** `Failed Logins by Username`

**Search Query:**

```spl
source="ssh_logs_new.json" host="LinuxNew" sourcetype="_json" event_type="Failed SSH Login"
| top username
```
<img width="1919" height="967" alt="57" src="https://github.com/user-attachments/assets/bc4808bb-48ee-4960-b8e2-e82a183b076d" />
<img width="1919" height="966" alt="58" src="https://github.com/user-attachments/assets/4796bb11-0e6b-44bf-9070-60714035774a" />
<img width="1919" height="968" alt="59" src="https://github.com/user-attachments/assets/42b4c6c5-055e-42fe-9eef-1c096c238fd3" />
<img width="1919" height="969" alt="60" src="https://github.com/user-attachments/assets/e5db006d-1cc7-49a2-9ad6-89b405944ca2" />
<img width="1919" height="966" alt="61" src="https://github.com/user-attachments/assets/8863b9da-5cde-4e14-9900-70acb1598597" />
<img width="1919" height="965" alt="62" src="https://github.com/user-attachments/assets/0484e1a1-c47e-4d0e-a639-b4c464ed0364" />
<img width="1919" height="961" alt="63" src="https://github.com/user-attachments/assets/41b49ae6-2a61-4bb1-aae5-82a66ede54a6" />
<img width="1919" height="967" alt="64" src="https://github.com/user-attachments/assets/d96d7cb8-c037-47d8-9a6d-60eaae35d213" />

---

### 2️⃣ Possible Brute Force Attempts by IP Address

* **Panel Type:** Statistics Table
* **Time Picker:** `time_range`
* **Title:** `Possible Brute Force by IP Address`

**Search Query:**

```spl
source="ssh_logs_new.json" host="LinuxNew" sourcetype="_json" event_type="Multiple Failed Authentication Attempts"
| top id.orig_h
```
<img width="1919" height="966" alt="65" src="https://github.com/user-attachments/assets/ef32d8f1-e463-44ec-b757-f0d78abac1cf" />
<img width="1919" height="968" alt="66" src="https://github.com/user-attachments/assets/163db51f-5984-4650-bf1b-8ef9f2f4328a" />
<img width="1919" height="965" alt="67" src="https://github.com/user-attachments/assets/8eff2695-f553-4608-a15b-2b289b9f0765" />
<img width="1919" height="966" alt="68" src="https://github.com/user-attachments/assets/eb67e586-887d-42f3-820e-41c7665dfb72" />
<img width="1919" height="967" alt="69" src="https://github.com/user-attachments/assets/1adb992b-7735-4d00-8aa4-e3ed7dee1a40" />
<img width="1919" height="965" alt="70" src="https://github.com/user-attachments/assets/3f17a550-3fe0-49ef-8289-53096af9cbdd" />
<img width="1919" height="963" alt="71" src="https://github.com/user-attachments/assets/650fefad-a36b-4a85-9b14-51231d2ee6d3" />
<img width="1919" height="965" alt="72" src="https://github.com/user-attachments/assets/cb113e50-7e8b-4a3e-b661-f4a744552d8e" />

---

## 🌍 Task 3: Visualizing Brute Force Attacks Using Geo-Location

### Goal

Identify **geographical sources** of brute-force SSH attacks.

---

### 1️⃣ Brute Force Attack with Geo-Location

* **Panel Type:** Choropleth Map
* **Time Picker:** `time_range`
* **Title:** `Brute Force Attack with Geo-Location`

**Search Query:**

```spl
source="ssh_logs_new.json" host="LinuxNew" sourcetype="_json" event_type="Multiple Failed Authentication Attempts"
| table id.orig_h
| iplocation id.orig_h
| stats count by Country
| geom geo_countries featureIdField="Country"
```
<img width="1919" height="968" alt="73" src="https://github.com/user-attachments/assets/fa90f069-f76f-46b2-a5da-01dbcf110870" />
<img width="1919" height="965" alt="74" src="https://github.com/user-attachments/assets/f1d9a840-649f-4c48-8a59-f3b1bec60e8f" />
<img width="1919" height="968" alt="75" src="https://github.com/user-attachments/assets/c122d06d-491e-4071-bbe3-3764bcb477f2" />
<img width="1919" height="967" alt="76" src="https://github.com/user-attachments/assets/d83b80ce-20c8-4b2e-ae7b-7de5eb51337f" />
<img width="1919" height="967" alt="77" src="https://github.com/user-attachments/assets/fd9f373c-5a6b-458e-80f8-56e6840f39a5" />
<img width="1919" height="968" alt="78" src="https://github.com/user-attachments/assets/a4d341fe-2929-42f2-9700-52698bde0f89" />
<img width="1919" height="966" alt="79" src="https://github.com/user-attachments/assets/788a8d6d-00fe-4962-acb9-6ffec6c645c7" />
<img width="1919" height="968" alt="80" src="https://github.com/user-attachments/assets/ddb8cf73-26e4-42a0-8399-d76e3c72f9d7" />

---

## 🚀 Key Outcomes

* Centralized SSH authentication monitoring
* Early detection of brute-force attacks
* Improved visibility using geo-location analysis
* Consistent time-based analysis across panels

---

## 🛡️ Security Use Case

This dashboard can be used by:

* SOC Analysts
* Blue Teams
* System Administrators
* Cybersecurity Students

to **detect unauthorized access attempts** and **respond to SSH-based attacks efficiently**.

![Uploading 81.png…]()



