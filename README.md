
---

# Backend Developer - Practical Test

### `Duration → max 24 hours `

# **Instruction**

1. **Read** the requirements in detail.
2. **Develop and upload** to your new public repo.
3. **Document** the following in your `README.md`:
   - How to set up the project locally (including migrations, seeders, and storage links).
   - How to run the project (include commands for serving and running tests).
   - How to interact with the API (if you completed the API endpoints).
4. **Send us** the repo URL back.
5. **Commit** 1st when you start and end so we know first and last as the time tracker.

---

## Requirements

### **1. Authentication**
- `implement` **Basic Authentication** using Laravel Breeze or Jetstream (instead of the default `make:auth`).
- `ensure` **RBAC**: only users with the role of **Administrator** can manage companies and employees.
  - seed the database with an initial user:
    - Email: `admin@admin.com`
    - Password: `password`
    - Role: `Administrator`

### **2. CRUD**
- `implement` CRUD operations for two models: **Company** and **Employee**.

#### **Companies:**
- `name`, `email`, `logo`, `website`

#### **Employees:**
- `name`, `email`, `phone`, `profile`, `company_id`

### **3. Additional Features:**
1. **File Handling for Logos and Profiles:**
   - `store` images in the `storage/app/public` directory.
   - `ensure` they are accessible via a public URL `/storage`.
   - `resize` uploaded logos automatically  to ensure they meet the minimum size requirement.
   - `use` Laravel Image Processing, e.g., `intervention/image`.

2. **Implement Eloquent Relationships**

3. **Form Validation:**
   - `use` **Form Requests** to handle validation logic with your rules

4. **Search and Filtering:**
   - `add` the ability to **search and filter** the Companies and Employees list.
   - `implement` search functionality on the name, email, and website fields for companies and on name, email, and phone for employees.

5. **Pagination:**
   - `use` Laravel’s **pagination** to display both.
   - `ensure` the pagination works with the search and filter functionality.

6. **Role-Based Dashboard:**
   - `create` a simple dashboard for administrators that shows:
     - total number of companies and employees.
     - list of recent companies added.

### **4. API Endpoints (Bonus Task)**
- `create` **RESTful API** endpoints for managing companies and employees:
  - `GET /api/companies`
  - `POST /api/companies`
  - `PUT /api/companies/{id}`
  - `DELETE /api/companies/{id}`
- `use` **API Token Authentication** (Laravel Passport or Sanctum)
- `ensure` proper error handling and validation for each API endpoint

### **5. Testing**
- `implement` **unit** and **feature tests** to cover the main functionality.
- at a minimum, tests should cover:
  - company and employee creation.
  - validation failures for invalid input (e.g., incorrect email formats, missing required fields).
  - Role-based access control (ensuring only admins can manage data).

---

### **Expected Skills**

- Coding Proficiency and Clean Architecture
- Understanding of Laravel Framework
- Best practices for security, especially around authentication and file handling
- Optimization Skill
- Documentation Skill
- **Bonus**: API development and documentation

### **Notes**

- This project is not for business flows. You don't need to consider for that.
- This project is intended for **Coding Skill** only.
- You have to write meaningful git commits.
- You can improve your code as much as you can, **we will consider as bonus points**.