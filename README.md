# **Gemini-Powered Q&A and Vision Chatbot - Project Overview**

## **1. Introduction**
This project consists of **Streamlit-based chat applications** utilizing **Google's Gemini AI models** for:
- **Q&A Chatbot** (`app.py`, `chat.py`, `qachat.py`)
- **Vision-based Q&A** (`vision.py`)

Each app provides an interactive UI where users can input questions, receive AI-generated responses, and maintain chat history.

---

## **2. Tech Stack**
- **Frontend**: Streamlit (for UI)
- **AI Model**: Google Gemini Pro / Gemini Vision API
- **Backend**: Python with Generative AI API
- **Environment Management**: dotenv (for API key handling)

---

## **3. Application Breakdown**
### **A. Q&A Chatbot (`app.py`, `chat.py`, `qachat.py`)**
#### **Features**
✅ Accepts text-based user queries  
✅ Sends queries to **Google Gemini Pro API**  
✅ Displays AI-generated responses  
✅ Supports **streaming responses** (`chat.py`, `qachat.py`)  
✅ Maintains **chat history** (`qachat.py`)  

#### **Workflow**
1. User inputs a question in **Streamlit UI**.
2. The query is sent to **Gemini API** for processing.
3. AI-generated response is returned and displayed in real time.
4. **Chat history is stored and displayed** (`qachat.py`).

---

### **B. Vision-based Q&A (`vision.py`)**
#### **Features**
✅ Accepts **image uploads**  
✅ Processes images with **Gemini Pro Vision API**  
✅ Generates descriptions & answers based on image content  
✅ Allows optional **text prompts** along with images  

#### **Workflow**
1. User uploads an **image** in the Streamlit UI.
2. (Optional) User enters a **text prompt** for additional context.
3. The image (and prompt, if provided) is sent to **Gemini Vision API**.
4. AI processes the image and returns insights.
5. The response is displayed to the user.

---

## **4. API Integration**
Each application integrates with **Google Gemini AI** via:
- `genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))`
- Uses `GenerativeModel("gemini-pro")` for text.
- Uses `GenerativeModel("gemini-pro-vision")` for images.

---

## **5. Deployment**
- **Local Deployment**: Run with `streamlit run app.py`
- **Cloud Deployment**: Deploy on **Streamlit Sharing**, **Google Cloud Run**, or **AWS Lambda**.

---

## **6. Next Steps**
🚀 Improve response formatting with Markdown rendering  
🚀 Enhance UI with custom **Streamlit components**  
🚀 Add **multi-file support** in vision-based chatbot  
