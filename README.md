Internship Recommendation System

This project is a web-based internship recommendation system built using Flask, Python, and machine learning techniques. It recommends internships to students based on their skills and preferred location. The system uses a TF-IDF vectorizer and cosine similarity to match user input with internship data.

Features:
- User Registration and Login: Students can register and log in using their email.
- Internship Recommendation: The system recommends internships based on the student's skills and preferred location.
- CSV Data Storage: Student and internship data are stored in CSV files for simplicity.
- TF-IDF and Cosine Similarity: The recommendation engine uses TF-IDF vectorization and cosine similarity to find the best matches.

Installation:
1. Navigate to the repository:
   Bash
   cd internship-recommendation-system
2. Install dependencies:
   bash
   pip install -r requirements.txt
3. Prepare the data:
   - Ensure you have two CSV files:
     - `intern.csv`: Contains internship details (e.g., Profile, Company, Location, Skills Required, etc.).
     - `Student_data.csv`: Contains student registration details (e.g., Name, Email, Skills, Location, etc.).
 
  - Update the paths to these files in `app.py`:
     python
     internship_data_path  =  " D:\InternshipBuddies\inter.csv"
     student_data_path  =   " D:\InternshipBuddies\Student_data.csv"
4. Run the application:
   bash
   python app.py
5. Access the application:
   Open your browser and go to `http://127.0.0.1:5000/`.

Usage:
1. Home Page:
   - Students can log in using their email or register if they are new users.

 
 

Logo:
 
2. Registration Page:
   - New users can register by providing their details (e.g., name, email, skills, location, etc.).
3. Login Page:
 
-Students log in using their registered email ID.
o	If the email ID is not registered, they are prompted to register first.
-Input Skills and Location:
o	After logging in, students provide their skills and preferred location.

4. Recommendation Page:
   - After logging in, students can view internship recommendations based on their skills and preferred location.

 

 File Structure:

- `app.py`: The main Flask application with routes and recommendation logic.
- `model.py`: Contains the recommendation engine logic (TF-IDF and cosine similarity).
- `user.py`: Handles user registration, login, and data retrieval from the CSV file.
- `templates/`: Contains HTML templates for the web pages (e.g., `index.html`, `register.html`, `recommendation.html`).
- `internship_data.csv`: Stores internship data.
- `student_data.csv`: Stores student registration data.



Code Overview:
`model.py`
- Function: `recommend_internships`
  - Takes internship data, user skills, and location as input.
  - Combines skills and location into a single feature for recommendation.
  - Uses TF-IDF vectorization and cosine similarity to recommend the top 5 internships.

`app.py`
- Routes:
  - `/`: Home page for login.
  - `/register`: Registration page for new users.
  - `/recommend`: Displays recommended internships for logged-in users.
- Session Management: Stores user email, skills, and location in the session for personalized recommendations.

`user.py`
- Functions:
  - `is_user_registered`: Checks if a user is already registered.
  - `register_user`: Registers a new user by appending their data to the CSV file.
  - `validate_login`: Validates user login by checking if the email exists in the CSV file.



Dependencies:
- Flask
- Pandas
- Scikit-learn

Future Improvements:

- Add a database (e.g., SQLite, PostgreSQL) for better data management.
- Implement user profiles and allow users to update their skills and preferences.
- Add more advanced recommendation algorithms (e.g., collaborative filtering).

Contact Information:
   github link  : https://github.com/SuhainaG/InternshipBuddies/upload
   linkedin link :  linkedin.com/in/suhaina-g-2a083925a
   Contact Number :  8088672153
  Whatsapp Number :    7204384182
