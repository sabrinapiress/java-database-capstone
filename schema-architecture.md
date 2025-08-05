## Section 1: Architecture Overview

This Spring Boot application uses both MVC and REST controllers. Thymeleaf templates are used for the Admin and Doctor dashboards, while REST APIs serve all other modules. The application interacts with two databases—MySQL (for patient, doctor, appointment, and admin data) and MongoDB (for prescriptions). All controllers route requests through a common service layer, which in turn delegates to the appropriate repositories. MySQL uses JPA entities, while MongoDB uses document models.


## Section 2: Data Flow and Numbered Control

1. The user accesses the Admin or Appointment dashboards.
2. The action is routed to the appropriate Thymeleaf or REST controller.
3. The controller calls the corresponding service layer.
4. The service layer processes the required business logic.
5. The service layer interacts with JPA repositories (MySQL) or document models (MongoDB).
6. Data is retrieved or updated in the databases as needed.
7. The response is sent back to the user via Thymeleaf template or as a REST response.