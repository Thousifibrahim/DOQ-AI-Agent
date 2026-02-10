
<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.38-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-0.3-1C3C3C?style=for-the-badge&logo=chainlink&logoColor=white)](https://www.langchain.com/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

*Chat with your PDFs using AI - Beautiful UI meets powerful language models*

</div>

##  DOQ AI Assistant

###  What This Does

Upload any PDF document and ask questions about its content. The AI reads, understands, and answers your questions in natural language - perfect for research papers, books, reports, or any document you need to analyze quickly.


#
### ✨ Key Features

- **Upload & Ask** - Drop a PDF, ask questions, get instant answers
- **AI-Powered** - Uses advanced language models via Hugging Face
- **Modern UI** - Glassmorphic design with dark/light mode toggle
- **Responsive** - Works seamlessly on desktop and mobile
- **Docker Ready** - One-command deployment
- **Secure** - API keys safely managed via environment variables

#

### 🚀 Quick Start :

### **Prerequisites**

- Python 3.9+ installed
- Hugging Face account → [Get API Token](https://huggingface.co/settings/tokens)
- Docker (optional, for containerized deployment)

### **Installation**

1. **Clone the repository**
```bash
git clone https://github.com/Thousifibrahim/pdf_qa_chatbot.git
cd pdf_qa_chatbot
```

2. **Set up environment**
```bash
# Create virtual environment
python -m venv venv

# Activate it
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt
```

3. **Configure API token**

Create a `.env` file in the project root:
```
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

4. **Add background image (optional)**

Place your image in `assets/background.jpg`

5. **Run the app**
```bash
streamlit run app.py
```

Open your browser to `http://localhost:8501`

#

### 🐳 Docker Setup

**Using Docker Compose (Recommended):**
```bash
docker-compose up
```

**Or build and run manually:**
```bash
# Build image
docker build -t pdf-ai-assistant .

# Run container
docker run -p 8501:8501 pdf-ai-assistant
```

Access at `http://localhost:8501`


#
### 📁 Project Structure

```
pdf_qa_chatbot/
├── assets/
│   └── background.jpg          # Custom background
├── app.py                      # Main Streamlit app
├── qa_chain.py                 # LangChain Q&A logic
├── document_processor.py       # PDF processing
├── requirements.txt            # Dependencies
├── Dockerfile                  # Container config
├── docker-compose.yml          # Docker Compose setup
├── .env                        # API keys (not committed)
└── .gitignore                  # Git ignore rules
```


#
### 🛠️ Tech Stack

**Core Technologies:**
- **Streamlit** - Interactive web interface
- **LangChain** - LLM orchestration framework
- **Hugging Face** - Language model API
- **FAISS** - Vector similarity search
- **PyMuPDF** - PDF text extraction
- **Sentence Transformers** - Text embeddings

**Full Dependencies:**
```
streamlit==1.38.0
langchain==0.3.0
langchain-huggingface==0.1.0
langchain-community==0.3.0
pymupdf==1.24.9
faiss-cpu==1.8.0
sentence-transformers==3.1.1
transformers==4.44.2
torch==2.4.1
python-dotenv==1.0.1
```


#
### 🌐 Deployment

### **Deploy to Streamlit Cloud (Free)**

1. Push your code to GitHub
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud)
3. Create new app → Select your repo
4. Set environment variable: `HUGGINGFACEHUB_API_TOKEN`
5. Deploy! 🚀
#
### **Deploy to Render (Free)**

1. Push Docker image to Docker Hub:
```bash
docker login
docker tag pdf-ai-assistant yourusername/pdf-ai-assistant
docker push yourusername/pdf-ai-assistant
```

2. Create Web Service on [render.com](https://render.com)
3. Configure:
   - **Image:** `yourusername/pdf-ai-assistant`
   - **Port:** `8501`
   - **Environment Variables:** Add your Hugging Face token
4. Deploy!

#

## 🔧 Troubleshooting

**API Token Issues:**
- Verify token is set in `.env` file
- Get new token from [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)

**Docker Not Starting:**
```bash
# Check Docker is running
docker info

# Increase Docker resources (4GB RAM recommended)
# Docker Desktop → Settings → Resources
```

**Background Image Not Showing:**
- Ensure `assets/background.jpg` exists
- Check file permissions
- Try a different image format (PNG/JPG)

#
### 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit changes: `git commit -m 'Add AmazingFeature'`
4. Push to branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request
#
###  Contact & Connect

**Thousif Ibrahim**

[![GitHub](https://img.shields.io/badge/GitHub-Thousifibrahim-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Thousifibrahim)
[![Email](https://img.shields.io/badge/Email-contact.thousif+github@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contact.thousif+github@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Thousif%20Ibrahim-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thousif-ibrahim-29050421b)


**⭐ Star this repo if you find it helpful!**

*Made with ❤️ by Thousif Ibrahim*

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=Thousifibrahim.pdf_qa_chatbot)
