# Employee Management System

## HOW TO RUN THIS PROJECT
### FROM THE IDE
1. Open the project in an IDE like Eclipse.
2. Run the DBScript in MySQL to create the database and tables.  
   (Creating database is necessary since hibernate-update option is used: `spring.jpa.hibernate.ddl-auto = update`)
3. If you don’t want to run the file, change  
   `spring.jpa.hibernate.ddl-auto = update` → `spring.jpa.hibernate.ddl-auto = create-drop`  
   in `src/main/resources/application.properties`.
4. Check your database connection in `application.properties` and update if needed.
5. Go to `com.employee.management`.
6. Right-click on class `Application.java`.
7. Select “Run As → Java Application” in the IDE.
8. Confirm that the localhost server has started.
9. Open Postman on your system.
10. Try the URLs below to test the APIs:
   - `http://localhost:8080/employees`
   - `http://localhost:8080/departments`

### API ENDPOINTS
**Department**
- GET `/departments` → list all departments  
- GET `/departments/{id}` → get by ID  
- POST `/departments` → add new department  
- PUT `/departments/{id}` → update by ID  
- DELETE `/departments` → delete all  
- DELETE `/departments/{id}` → delete by ID  
- PATCH `/departments/{id}` → patch/update by ID  

**Employee**
- GET `/employees` → list all employees  
- GET `/employees/{id}` → get by ID  
- POST `/employees` → add new employee  
- PUT `/employees/{id}` → update by ID  
- DELETE `/employees` → delete all  
- DELETE `/employees/{id}` → delete by ID  
- PATCH `/employees/{id}` → patch/update by ID  

---

## ASSUMPTIONS
1. Database and tables are created in MySQL.
2. DepartmentID is a foreign key in the Employee table.
3. Department table must be populated before adding an employee.
4. Example JSON for POST request:
```json
{
  "employeeID": 2,
  "firstName": "Tim",
  "lastName": "Cook",
  "department": 3
}
```

---

## TECHNOLOGY STACK
- Java  
- Spring Boot  
- Eclipse IDE  
- MySQL Workbench  
- Postman API Tool

---

## DESIGN DISCUSSION
1. The Employee table has a foreign key DepartmentID.
2. Department must exist before assigning to an employee.
3. CRUD operations are handled by RESTful mappings.
4. Database connection is managed through `application.properties`.

---

## FUTURE ENHANCEMENTS
1. Add user authentication with roles (admin, employee).
2. Add UI for managing employee data.
3. Integrate with cloud database.

---

✨ **Developed by Aryan Nigam**  
🎓 B.Tech (Information Technology)  
📍 Dr. Ram Manohar Lohia Awadh University
