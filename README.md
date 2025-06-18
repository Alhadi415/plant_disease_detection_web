
🌿 Plant Disease Detection API

A simple web application built with Flask and Keras to detect whether a plant leaf is healthy or infected based on an uploaded image.

🚀 Features
•	Easy-to-use web interface
•	Upload an image to detect plant disease
•	Automatically downloads the trained model from Google Drive if not available locally
•	Returns prediction as Healthy or Infected

📦 Requirements
Make sure you have Python 3.7+ installed. Then, install the required packages:
pip install -r requirements.txt
Or manually install:
pip install flask tensorflow pillow gdown

🧠 Model Download
If the model file plant_disease_model_final.h5 is not found in the project directory, it will be automatically downloaded from Google Drive using this ID:
1RGKYGHs4-reK7I52ZoqKgk-MpPymZvfa
▶️ How to Run
Start the Flask server with:
python app.py
Then open your browser and go to:
http://127.0.0.1:5000/
🧬 How It Works
1.	The user uploads a plant leaf image through the web interface.
2.	The image is resized to 256x256 and preprocessed.
3.	The preprocessed image is passed to the trained deep learning model.
4.	The model predicts whether the plant is healthy or infected.
5.	The result is returned as JSON or shown on the web page.
________________________________________
📁 Project Structure
.
├── app.py                        # Main Flask application
├── plant_disease_model_final.h5 # Trained model (auto-downloaded if missing)
├── templates/
│   └── index.html               # Web interface
________________________________________
📤 API Endpoint
POST /predict
•	Body: Form data with an image file (key: file)
•	Response: JSON object
Example Response
{
  "result": "Healthy"
}
________________________________________
⚙️ Prediction Threshold
•	If model output > 0.7 → Infected
•	Otherwise → Healthy
________________________________________
📄 License
This project is intended for educational and experimental purposes. Feel free to modify and use it.

