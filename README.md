# EatSmart Backend

EatSmart is an AI-powered personalized meal planning application.  
This repository contains the backend server built with **Java Spring Boot** and **Maven**,  
responsible for managing user profiles, meal planning, grocery lists, nutrition tracking, and more.

---

## 🚀 Project Scope

- User onboarding with dietary goals and restrictions
- AI-driven meal generation
- Meal plan approval and tracking
- Auto-generation of daily grocery lists
- Saved recipes management
- Nutrition goals and streak tracking
- Secure Supabase authentication
- Clean API design for mobile app (React Native)

---

## 📦 Folder Structure

```plaintext
src/main/java/com/eatsmart/
🔼️ config/           # Application configurations (Database, CORS, etc.)
🔼️ controller/       # REST API Controllers
🔼️ dto/              # Request and Response data transfer models
🔼️ entity/           # JPA Entity classes mapped to PostgreSQL tables
🔼️ exception/        # Global error handling
🔼️ repository/       # Database access layer (Spring Data JPA)
🔼️ security/         # JWT Authentication setup (future)
🔼️ service/          # Business logic and service classes
🔼️ util/             # Utility/helper classes
🔼️ EatSmartApplication.java # Main Spring Boot Application Entry
```

Resources:
```plaintext
src/main/resources/
🔼️ application.yml    # Spring Boot application configuration
🔼️ db/migration/      # Flyway SQL migration scripts
```

---

## 🌐 API Endpoints

| Method | URL | Description |
|:---|:---|:---|
| `GET` | `/api/user/profile` | Fetch current user's profile |
| `POST` | `/api/user/setup` | Setup user goals and restrictions |
| `PATCH` | `/api/user/update` | Update user profile |
| `POST` | `/api/meal/generate` | Generate AI-based meal plan options |
| `POST` | `/api/meal/approve` | Approve today's meal plan |
| `GET` | `/api/meal?date=YYYY-MM-DD` | Fetch meals planned for a specific day |
| `POST` | `/api/grocery/generate` | Generate grocery list based on today's meals |
| `GET` | `/api/grocery?date=YYYY-MM-DD` | Fetch grocery list for a day |
| `PATCH` | `/api/grocery/mark/{itemId}` | Mark grocery item as available |
| `GET` | `/api/recipes/saved` | Fetch saved recipes |
| `POST` | `/api/recipes/save` | Save a new recipe |
| `GET` | `/api/goals/progress` | Fetch user's nutrition and goal tracking |

---

## ⚙️ Technology Stack

- Java 17
- Spring Boot 3
- Maven
- PostgreSQL (Supabase DB)
- Flyway (for database migrations)
- Lombok (for reducing boilerplate)
- OpenAI API (for AI meal suggestions)

---

## 🛠️ Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/SufiaAshraf/eatsmart-backend.git
   cd eatsmart-backend
   ```

2. Update `src/main/resources/application.yml` with your Supabase database credentials.

3. Build and run the project:
   ```bash
   mvn spring-boot:run
   ```

4. Access the app:
    - Local: [http://localhost:8082/](http://localhost:8082/)
    - Test API: [http://localhost:8082/api/user/profile](http://localhost:8082/api/user/profile)

---

## 🧐 Future Enhancements

- Family Mode support (multiple users under one account)
- Grocery delivery API integrations (Blinkit, Flink, etc.)
- Subscription plans (Premium meal plans)
- Nutrition-based recommendations (auto-adjusting based on progress)
- Admin dashboard for managing recipes and meals
- Push notifications for meal reminders

---

