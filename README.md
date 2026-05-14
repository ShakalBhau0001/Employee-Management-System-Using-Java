## 👨‍💼 Employee-Management-System-Using-Java (Command Line Interface)

## 📘 Overview
**Employee Management System** is a Java-based application to manage employee records.  
It uses JDBC to connect to a database and allows operations such as adding, updating, deleting, and viewing employees.

## 🧰 Prerequisites
- Java JDK 8 or above  
- Eclipse IDE for Enterprise Java and Web Developers
- Oracle Database or any other relational DB  
- `ojdbc8.jar` JDBC driver  
- **Employee Management System** project source code  

## ⚙️ Setup Guide

### 1️⃣ Install Eclipse IDE
1. Download **Eclipse IDE for Enterprise Java and Web Developers**
2. 👉 **[Eclipse Download Link](https://www.eclipse.org/downloads/packages/release/2025-12/r)**
3. Select **Windows x86_64** and download the ZIP version. 
4. After downloading, locate this file:  
   ```
   eclipse-java-2025-12-R-win32-x86_64.zip
   ```  
5. Extract the ZIP file:
   - Right-click on it  
   - Choose **“Extract All…”**
   - You’ll get a folder named **`eclipse`**
6. Open the folder and **double-click `eclipse.exe`** to launch the IDE.

### 2️⃣ Create Employee Management System Java Project
1. File → New → Java Project  
2. Enter project name: `Employee Management System`  
3. Click Finish  

### 3️⃣ Add JDBC Driver (`ojdbc8.jar`)
1. Right-click project → Build Path → Configure Build Path  
2. Go to **Libraries** tab  
3. Click "**Add External JARs**"  
4. Select `ojdbc8.jar`  
5. Click Apply and Close  

## 🧩 JDBC Setup for Employee Management System
Employee Management System supports these operations:
- Add Employee  
- View Employee  
- Update Employee  
- Delete Employee  

### 🔌 Database Connection File

```java
ConnectionEstablishment.java

import java.sql.*;
import oracle.jdbc.OracleDriver;

public class ConnectionEstablishment {
	public static void main(String[] args) throws Exception {
		DriverManager.registerDriver(new OracleDriver());
		Connection con = DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:XE","test","test");
    System.out.println("Connection Established Successfully");
		con.close();
	}
}

```

---

## 🧠 SQL Commands
Before running the Java code, create a user in Oracle Database:

```sql
CREATE USER test IDENTIFIED BY test;
GRANT dba TO test;
```

---

## ✅ Summary

| Step | Description                    |
| ---- | ------------------------------ |
| 1️⃣  | Install Eclipse IDE            |
| 2️⃣  | Create Employee Management System project             |
| 3️⃣  | Add JDBC driver                |
| 4️⃣  | Create JDBC classes            |
| 5️⃣  | Run Employee Management System application            |
| 💾   | Create database user and table |


---

## 🪪 Author

> **Creator: Shakal Bhau**

> **GitHub: [ShakalBhau0001](https://github.com/ShakalBhau0001)**

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

---
