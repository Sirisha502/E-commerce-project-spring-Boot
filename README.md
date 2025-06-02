# E-commerce-project-spring-Boot
# 🛒 E-Commerce Project - Spring Boot (Old Version)

A basic e-commerce application built with **Spring Boot**, **JSP**, **Hibernate**, and **MySQL**. This project follows the traditional **MVC architecture** and is designed for educational and demo purposes.

---

## ⚠️ Known Issue (Old Version)

- ❌ **Inefficient Database Access**  
  In the previous version, a new connection to the database was opened and closed on every single access. This led to performance issues and unnecessary load on the database.

---

## ✅ New Version Highlights

The updated version introduces a number of architectural improvements and bug fixes:

- 🔧 **Hibernate Configuration Added**  
  Automatically creates the database schema and tables when the application starts.

- ♻️ **Service Layer Added**  
  Reusable service classes make the logic cleaner and more modular.

- 🗂️ **DAO Layer Implemented**  
  DAO classes now handle all direct database interactions.

- 🐞 **Bug Fixes**  
  - Product image upload issues
  - Endpoint handling
  - Spring Security configuration

- 💻 **IDE Compatibility**  
  Now fully supports both **Eclipse** and **IntelliJ IDEA**.

- 🛠️ **Codebase Refactored**  
  Fully redesigned for better structure, reusability, and maintainability.

> ⚠️ **Disclaimer**: Active development is ongoing on this branch. Expect minor bugs in some endpoints and the cart logic is still in progress.

---

## 🚀 Quickstart

### 🧱 Prerequisites

- Java 17+
- Maven
- MySQL or MariaDB

### 📦 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/jaygajera17/E-commerce-project-springBoot.git
   cd E-commerce-project-springBoot
````

2. **Open the Project in IDE**

   * Preferred: IntelliJ IDEA
   * Also works in: Eclipse

3. **Make Sure the Project is Recognized as a Maven + Spring Boot Project**

4. **Configure Working Directory (for IntelliJ)**

   * Go to **Run > Edit Configurations**
   * Select `JtSpringProjectApplication`
   * Change the **Working Directory** to: `$MODULE_WORKING_DIR$`
   * Click **Apply** and **OK**

5. **Set Up Database Configuration**

   Open `src/main/resources/application.properties` and add:

   ```properties
   db.url=jdbc:mysql://<your-db-host>:<port>/ecommjava?createDatabaseIfNotExist=true
   db.username=<your-db-username>
   db.password=<your-db-password>
   ```

   > ⚠️ **Tip:** Avoid using `root` as your DB user. Use a user with limited privileges.

   * If you see this error:

     ```
     java.lang.IllegalArgumentException: Could not resolve placeholder 'db.driver'
     ```

     Update your `mysql-connector-java` version in `pom.xml` according to your MySQL version and reload Maven.

6. **Seed the Database**

   Run the provided `basedata.sql` file to insert initial data like admin and user accounts.

7. **Run the Project**

   Run `JtSpringProjectApplication.java` as a Spring Boot app.

8. **Visit in Browser**

   Open: [http://localhost:8080](http://localhost:8080)

---

## 🔐 Login Credentials

If you’ve imported the `basedata.sql`:

| Role  | Username | Password |
| ----- | -------- | -------- |
| Admin | admin    | 123      |
| User  | lisa     | 765      |

---

## 🗂️ Directory Structure Overview

* **Model**: Java classes that represent the data structure and database schema.
* **View**: JSP files under `src/main/webapp/views` responsible for rendering the UI.
* **Controller**: Handles HTTP routes and uses `ModelAndView` to send data to views.

### Example:

```java
@GetMapping("/login")
public String adminlogin() {
    return "adminlogin"; // Loads src/main/webapp/adminlogin.jsp
}
```

---

## 🌍 Key Endpoints

| URL                 | Purpose                  |
| ------------------- | ------------------------ |
| `/`                 | Home page                |
| `/register`         | User registration        |
| `/admin/products`   | Admin: View/Add products |
| `/admin/customers`  | Admin: View customers    |
| `/admin/categories` | Admin: View categories   |
| `/admin/Dashboard`  | Admin dashboard          |

---

## 🛠 Web Directory Fix (Views Not Found)

Spring Boot may not detect `src/main/webapp/views` by default.

### IntelliJ IDEA Fix:

1. Go to **Run > Edit Configurations**
2. Select `JtSpringProjectApplication`
3. Set **Working Directory** to `$MODULE_WORKING_DIR$`
4. Apply and rerun the app

---

## 📚 Helpful Links

* [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/)
* [Maven Docs](https://maven.apache.org/guides/index.html)
* [Spring MVC Guide](https://spring.io/guides/gs/serving-web-content/)
* [Spring REST Guide](https://spring.io/guides/gs/rest-service/)
* [Spring Security Reference](https://docs.spring.io/spring-security/reference/index.html)

---

## 📸 Preview

> *(You can add a screenshot or demo GIF here)*

---

## 🤝 Contributing

Pull requests and bug reports are welcome. If you find any issues, feel free to open an [issue](https://github.com/jaygajera17/E-commerce-project-springBoot/issues).

---

## 📌 License

This project currently does not have a license and is intended for educational/demo use only.

```

---

### ✅ To Use:
1. Create or replace the `README.md` file in your GitHub repository root.
2. Paste the above code into it.
3. Commit and push to GitHub.

Would you like me to generate this as a downloadable file or create a preview of how it will look on GitHub?
```
# WorkFlow
![image](https://github.com/user-attachments/assets/68a02778-3124-4ee6-8947-a65e8a4bfcea)


