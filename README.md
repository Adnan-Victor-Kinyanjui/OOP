# Recipe Finder — Object-Oriented Programming Project

## Project Overview

**Recipe Finder** is an interactive application designed to help users discover and view cooking recipes based on ingredients they have.
The project demonstrates **core Object-Oriented Programming (OOP)** principles such as **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**.

The system features a simple and intuitive user interface (React frontend) connected to a **Spring Boot Java backend** that manages recipes and ingredients.

---

## Group Members

| Name          | Registration Number 
| ------------  | ------------------- | 
| Adnan Victor  | 190036              | 
| Angel Njora   | 182242              | 
| Krystal Kivui | 178886              | 

---

## Problem Statement

Cooking enthusiasts often struggle to decide what to prepare based on ingredients they already have.
**Recipe Finder** solves this by providing an easy-to-use system that:

* Stores and displays multiple recipes.
* Checks which ingredients are available or missing.
* Guides users through step-by-step cooking instructions.
* Allows users to suggest new recipes.

---

## Object-Oriented Design

### Classes Overview

#### 1. **Recipe**

* Represents a single recipe.
* Attributes: `id`, `title`, `List<Ingredient> ingredients`, `List<String> steps`.
* Demonstrates **encapsulation** through private fields and public getters/setters.

#### 2. **Ingredient**

* Represents an ingredient used in recipes.
* Attributes: `name`, `quantity`, `unit`.
* Supports **composition** — each recipe is composed of multiple ingredients.

#### 3. **RecipeRepository**

* Manages all recipes in the system (data storage).
* Methods:

  * `findAll()`
  * `findById(String id)`
  * `save(Recipe recipe)`
  * `deleteById(String id)`
* Demonstrates **abstraction** and **encapsulation** by hiding internal data management.

#### 4. **RecipeController**

* Handles client requests (GET, POST, DELETE).
* Demonstrates **polymorphism** through method overloading and interaction between classes.

---

## Features

View all recipes
View full recipe details (ingredients and steps)
Add available ingredients
Identify missing ingredients
Suggest new recipes
Modern UI styled with CSS

---

## OOP Concepts Used

| Concept           | Example                                                                      |
| ----------------- | ---------------------------------------------------------------------------- |
| **Encapsulation** | Private fields in `Recipe` and `Ingredient` classes with getters and setters |
| **Inheritance**   | Controller inherits behavior from Spring’s `@RestController` base            |
| **Polymorphism**  | Overridden methods in the repository and service handling recipe operations  |
| **Abstraction**   | Separation of logic between model, repository, and controller                |

---

## Technologies Used

* **Java 17** (Spring Boot Framework)
* **React (Vite)** – for frontend UI
* **HTML/CSS/JavaScript**
* **RESTful API Communication**
* **Maven** for backend build management

---

## How to Run

### Backend (Spring Boot)

1. Open the backend folder in **IntelliJ IDEA** or **VS Code**.
2. Run the `RecipeApplication.java` file.
3. Server starts at:
    `http://localhost:8080/api/recipes`

### Frontend (React + Vite)

1. Open a terminal in the `recipe-frontend` directory.
2. Run:

   ```bash
   pnpm install
   pnpm dev
   ```
3. Open your browser and visit:
   `http://localhost:5173/`

---



 Challenges Faced

* Integrating frontend with the backend API
* Managing state between components in React
* Understanding CORS configuration in Spring Boot
* Structuring code to demonstrate all OOP principles



Lessons Learned

* Gained hands-on experience applying OOP principles in a real-world system.
* Learned how to connect a Java backend with a modern JavaScript frontend.
* Improved team collaboration and version control skills.



Submission Contents

The submitted ZIP file contains:

```
RecipeFinderProject.zip
│
├── /src/main/java/com/example/recipe/
│   ├── model/
│   │   ├── Recipe.java
│   │   └── Ingredient.java
│   ├── repository/
│   │   └── RecipeRepository.java
│   ├── controller/
│   │   └── RecipeController.java
│   └── RecipeApplication.java
│
├── /recipe-frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── components/
│   │       ├── RecipeList.jsx
│   │       └── RecipeDetail.jsx
│   └── package.json
│
├── README.md
└── Presentation.ppt
