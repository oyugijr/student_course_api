# 🎓 Student-Course Management API

A modular FastAPI + MongoDB backend system for managing students, courses, and enrollments. Built with scalability, clarity, and developer productivity in mind.

---

## 🚀 Features

- 📘 Create and fetch student records
- 📗 Create and list courses
- 🔗 Enroll students in multiple courses (many-to-many)
- 🔍 Retrieve students along with their enrolled courses
- 🧩 Clean modular structure
- 🌐 Interactive API docs with Swagger UI

---

## 🛠 Tech Stack

- **Backend:** FastAPI (Python)
- **Database:** MongoDB Atlas (via PyMongo)
- **API Docs:** Swagger (via FastAPI)
- **Environment Config:** Python Dotenv

---

## 📁 Project Structure

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/your-username/student-course-api.git
cd student_course_api
2. Create and activate a virtual environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
3. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Add your MongoDB URI
Create a .env file in the root:

ini
Copy
Edit
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/?retryWrites=true&w=majority
5. Run the server
bash
Copy
Edit
uvicorn app.main:app --reload
Visit: http://127.0.0.1:8000/docs for Swagger UI.

📬 API Endpoints
Method	Endpoint	Description
POST	/students	Add a new student
GET	/students/{student_id}	Get student with enrolled courses
POST	/students/{id}/enroll	Enroll student in courses
POST	/courses	Add a new course

📦 Example Payloads
Add Student
json
Copy
Edit
{
  "name": "Alice",
  "studentId": 1001,
  "age": 21,
  "courseIds": ["CS101", "MATH204"]
}
Add Course
json
Copy
Edit
{
  "title": "Intro to AI",
  "courseId": "AI101",
  "instructor": "Dr. Smith"
}
Enroll Student
json
Copy
Edit
{
  "courseIds": ["CS101", "MATH204"]
}
🧠 Future Improvements
JWT-based user authentication

Admin dashboard with role-based access

Search and filter functionality

Docker support for deployment

CI/CD integration

📄 License
MIT License – free to use, modify, and share.

💬 Feedback or Contributions?
Feel free to fork, create issues, or submit a pull request! Contributions are welcome.

