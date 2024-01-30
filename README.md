# Recipe App API

Welcome to the Recipe App API repository! This project is a demonstration of an advanced backend REST API built using Python, Django (3.2), Django REST Framework (3.12), Docker, Postgres, and Test Driven Development (TDD).

## Overview

The Recipe App API is a backend application designed to manage recipes. It allows users to perform CRUD (Create, Read, Update, Delete) operations on recipes, upload and view images associated with recipes, and authenticate users.

## Features

- User authentication
- CRUD operations for recipe objects
- Filtering and sorting recipes
- Uploading and viewing images associated with recipes
- Dockerized development environment setup
- PostgreSQL database configuration
- Customization of the Django admin interface

## Getting Started

### Prerequisites

- Python
- Django
- Django Rest Framework
- PostgreSQL
- Docker

### Installation

To get started with the Recipe App API, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/JathinShyam/recipe-app-api.git
2. Navigate to the project directory:

   ```bash
   cd recipe-app-api
3. Create a virtual environment (optional but recommended):

   ```bash
   python3 -m venv venv
4. Activate the virtual environment:

- On Windows:

   ```bash
   venv\Scripts\activate
- On macOS and Linux:

   ```bash
   source venv/bin/activate
5. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
6. Set up the Docker development environment:

   ```bash
   docker-compose up -d --build
7. Create a superuser for accessing the Django admin interface:

   ```bash
   docker-compose run --rm app sh -c "python manage.py createsuperuser"
8. Access the Django admin interface and create some initial data:

- Open your web browser and go to <http://localhost:8000/admin>
- Log in with the superuser credentials created in the previous step

9. Start the development server:

   ```bash
   docker-compose up
10. Access the API endpoints:

- Open your web browser and go to <http://localhost:8000/api/>

## API Endpoints

### Authentication Endpoints

- (POST) **/api/user/create/** Create a new user account.
- (GET) **/api/user/me/** Check details of user.
- (PUT) **/api/user/me/** Update details of user account.
- (PATCH) **/api/user/me/** Partial update details of user account.
- (POST) **/api/user/token/** Create token, used for authentication.

### Recipe Endpoints

- **/api/docs/** For API Documentation and schema.
- (GET) **/api/recipe/ingredients/** List all recipe ingredients and also get filtered ingredients if we pass id params.
- (PUT) **/api/recipe/ingredients/{id}/** Update particular recipe ingredients.
- (PATCH) **/api/recipe/ingredients/{id}/** partial update of  particular recipe ingredients.
- (DELETE) **/api/recipe/ingredients/{id}/** Delete particular recipe ingredients.
- (GET) **​/api​/recipe​/recipes​/** List all recipes.
- (POST) **​/api​/recipe​/recipes​/** Create a new recipe.
- (GET) **/api/recipe/recipes/{id}/** Get a particular recipe.
- (PUT) **/api/recipe/recipes/{id}/** Update particular recipe.
- (PATCH) **/api/recipe/recipes/{id}/** partial update of particular recipe.
- (DELETE) **/api/recipe/recipes/{id}/** Delete particular recipe.
- (POST) **/api/recipe/recipes/{id}/upload-image/** upload image for particualr recipe.
- (GET) **/api/recipe/tags/** List all tags.
- (PUT) **/api/recipe/tags/{id}/** Update particular tag.
- (PATCH) **/api/recipe/tags/{id}/** partial update of particular tag.
- (DELETE) **/api/recipe/tags/{id}/** Delete particular tag.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.
