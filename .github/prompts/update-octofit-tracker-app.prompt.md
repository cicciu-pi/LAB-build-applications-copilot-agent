# Update Octofit Tracker Django App

Follow these steps to update the Django project/app files in `octofit-tracker/backend/octofit_tracker`:

## 1. Update `settings.py`
- Ensure the MongoDB connection uses Djongo and points to the correct database (`octofit_db`).
- Configure CORS to allow all origins, methods, and headers for development.

## 2. Update Core Django Files
- Update or create the following files to support users, teams, activities, and workouts:
  - `models.py`: Define models for User, Team, Activity, and Workout.
  - `serializers.py`: Create serializers for all models, converting ObjectId fields to strings as needed.
  - `views.py`: Implement API views for CRUD operations on all models.
  - `urls.py`: Route API endpoints for all resources and ensure `/api-root` exists and is accessible.
  - `admin.py`: Register all models for Django admin.
  - `tests.py`: Add tests for all API endpoints and models.

## 3. API Routing
- Ensure `urls.py` includes all API endpoints and `/api-root` is defined and working.

## 4. Best Practices
- Follow Django REST Framework conventions.
- Use the Codespace environment variable for allowed hosts if applicable.
- Test all endpoints with `curl` or similar tools.

---

**Do not start the Django server after making these updates.**
