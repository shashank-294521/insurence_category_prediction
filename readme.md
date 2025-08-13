# 🏥 Insurance Premium Category Prediction

This project predicts the **insurance premium category** (e.g., low, medium, high) based on user details such as age, BMI, lifestyle risk, city tier, occupation, and income.  

It consists of:
- **Backend:** FastAPI API for handling prediction requests.
- **Frontend:** Streamlit web interface for user input and displaying predictions.
- **ML Model:** Pre-trained scikit-learn pipeline saved as `model.pkl`.

---

## 📂 Project Structure

insurence_prediction/
│
├── app.py # FastAPI backend
├── frontend.py # Streamlit frontend
├── model.pkl # Pickled trained ML model
├── requirements.txt # Python dependencies
└── README.md # Project documentation

yaml
Copy
Edit

---

## ⚙️ Features

- **User Input Validation:**  
  Uses Pydantic models to validate age, weight, height, income, city, and occupation.

- **Computed Fields:**  
  Automatically calculates:
  - BMI (Body Mass Index)
  - Lifestyle Risk (based on smoking status and BMI)
  - Age Group
  - City Tier

- **Machine Learning Integration:**  
  Loads a pre-trained scikit-learn model to predict premium category.

- **Interactive Frontend:**  
  Simple Streamlit UI for user-friendly interaction.

---

## 🖥️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone <repo_url>
cd insurence_prediction
2️⃣ Create a virtual environment
bash
Copy
Edit
python -m venv venv
Activate it:

Windows (PowerShell):

bash
Copy
Edit
venv\Scripts\activate
Mac/Linux:

bash
Copy
Edit
source venv/bin/activate
3️⃣ Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
Example requirements.txt:

nginx
Copy
Edit
fastapi
uvicorn
streamlit
pandas
scikit-learn
requests
🚀 Running the Application
1️⃣ Start the FastAPI backend
bash
Copy
Edit
uvicorn app:app --reload
Backend will run at:

cpp
Copy
Edit
http://127.0.0.1:8000
Docs available at:

arduino
Copy
Edit
http://127.0.0.1:8000/docs
2️⃣ Start the Streamlit frontend
In a new terminal (same virtual environment):

bash
Copy
Edit
streamlit run frontend.py
Frontend will open in your browser at:

arduino
Copy
Edit
http://localhost:8501
📤 API Endpoint
POST /predict
Description: Predicts insurance premium category.
Request Body Example:

json
Copy
Edit
{
    "age": 30,
    "weight": 65.5,
    "height": 1.7,
    "income_lpa": 10.0,
    "smoker": false,
    "city": "Mumbai",
    "occupation": "Engineer"
}
Response Example:

json
Copy
Edit
{
    "predicted_category": "Medium"
}
📊 Model Details
Model File: model.pkl

Framework: scikit-learn

Pipeline Components: OneHotEncoder, ColumnTransformer, DecisionTreeClassifier, RandomForestClassifier (example)

Features Used: BMI, Age Group, Lifestyle Risk, City Tier, Income, Occupation

📝 Notes
The backend and frontend must run simultaneously for the app to work.

Ensure that model.pkl exists in the project root and is compatible with the installed scikit-learn version.

To avoid version mismatch errors, use the same scikit-learn version that was used during model training.

📜 License
This project is licensed under the MIT License.

yaml
Copy
Edit

---

If you want, I can also create a **`requirements.txt`** for your exact FastAPI + Streamlit + scikit-learn setup so anyone can install and run it without guessing package versions. That would make this README fully plug-and-play.








Ask ChatGPT
