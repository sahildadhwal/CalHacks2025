# 📚 LearnIt AI - Smart Syllabus Scheduler

> Transform your course syllabus into a personalized, AI-powered study schedule complete with YouTube video resources and interactive quizzes!

**🏆 CalHacks 2025 Project**  
**👥 Team:** Sahil Dadhwal, Vicky Kang, Mai Westfall

**🌐 Live Demo:** [calhacks2025-learnitai.up.railway.app](https://calhacks2025-learnitai.up.railway.app)

---

## 🎯 Problem Statement

**33% of first-generation students drop out** (Source: NCES)

While colleges offer financial aid, daycare, and counseling, students still struggle to manage their coursework effectively. LearnIt AI bridges this gap by providing personalized, AI-powered study schedules that adapt to individual learning needs.

---

## ✨ Features

### 📄 Smart Input Options
- **PDF Upload Support** - Direct syllabus PDF upload with text extraction
- **Text Input** - Paste syllabus content directly
- **File Support** - PDF, TXT, and Markdown files

### 🤖 AI-Powered Planning
- **Intelligent Scheduling** - Weekly and daily study plans using Groq's Llama 3.3 70B
- **Realistic Time Estimates** - 2-3 hour daily sessions
- **Progressive Difficulty** - Gradual complexity increase
- **Review Days** - Strategic review sessions before major topics

### 📺 Rich Learning Resources
- **YouTube Integration** - Curated video search links for each topic
- **Specific Search Terms** - Targeted educational content
- **Direct Links** - One-click access to video tutorials

### 🧠 Interactive Quizzes
- **Auto-Generated Questions** - Multiple choice quizzes for each major topic
- **Instant Feedback** - Immediate answer validation
- **Detailed Explanations** - Learn why answers are correct/incorrect

### 📊 Progress Tracking
- **Visual Progress Bar** - See your completion percentage
- **Persistent Storage** - Saves locally in your browser
- **Task Completion** - Mark days as complete
- **Statistics Dashboard** - Track weeks, hours, videos, and quizzes

### 📅 Export & Share
- **Calendar Export** - iCalendar (.ics) format for Google Calendar, Outlook, etc.
- **Print Schedule** - Printer-friendly format
- **Share Functionality** - Share your study plan with friends

### 🎨 Modern User Experience
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Intuitive Interface** - Clean, easy-to-navigate UI
- **Smooth Animations** - Professional transitions and effects
- **Dark/Light Accents** - Modern gradient design

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- pip (Python package manager)
- **Groq API Key** (FREE - see setup below)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/sahildadhwal/CalHacks2025.git
cd CalHacks2025
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables**

Create a `.env` file in the root directory:
```bash
GROQ_API_KEY=your_groq_api_key_here
```

4. **Run the application**
```bash
python app.py
```

5. **Open in browser**
```
http://localhost:5001
```

---

## 🔑 Getting Your FREE Groq API Key

LearnIt AI uses Groq's lightning-fast AI inference API (powered by Llama 3.3 70B). Here's how to get your free API key:

### Step 1: Sign Up
1. Go to [console.groq.com](https://console.groq.com)
2. Click **"Sign Up"** or **"Get Started"**
3. Create a free account (no credit card required!)

### Step 2: Generate API Key
1. After signing in, navigate to [console.groq.com/keys](https://console.groq.com/keys)
2. Click **"Create API Key"**
3. Give it a name (e.g., "LearnIt AI")
4. Copy the generated key (it will look like `gsk_...`)

### Step 3: Add to Your Project

**Option A: Environment Variable (Recommended)**
```bash
# Create .env file
echo "GROQ_API_KEY=your_key_here" > .env
```

**Option B: Web Interface**
1. Start the app without an API key
2. Click **"Change Key"** in the API Status section
3. Paste your key and click **"Save"**
4. The key will be stored in your browser's local storage

### Why Groq?
- ⚡ **Fastest inference** - Up to 10x faster than alternatives
- 🆓 **Generous free tier** - No credit card required
- 🧠 **Powerful models** - Llama 3.3 70B Versatile
- 🎯 **JSON mode** - Perfect for structured output
- 🌐 **Great API** - Simple, well-documented

---

## 📖 How to Use

### 1. Upload Your Syllabus

**Option A: Upload File**
- Drag and drop your syllabus PDF
- Or click to browse and select a file
- Supports PDF, TXT, and Markdown files

**Option B: Paste Text**
- Copy your syllabus content
- Paste directly into the text area

### 2. Configure Settings

**Course Duration**
- Select from 4 to 16 weeks
- Default: 10 weeks

**Start Date**
- Choose when you want to begin
- Default: Today

### 3. Generate Schedule

1. Click **"Generate Study Plan"**
2. Wait 10-20 seconds for AI processing
3. View your personalized schedule!

### 4. Use Your Schedule

**Weekly View**
- Click week headers to expand/collapse
- See overview for each week

**Daily Breakdown**
- View daily topics and objectives
- See estimated study hours
- Access YouTube video resources
- Take interactive quizzes
- Mark days as complete

**Track Progress**
- Visual progress bar shows completion
- Progress saved automatically
- Export to calendar apps
- Print or share your schedule

---

## 🏗️ Architecture

```
┌─────────────┐
│ User Starts │
└──────┬──────┘
       │
       ▼
┌─────────────────────┐      ┌──────────────────┐
│ Upload Syllabus     │      │ Set Preferences  │
│ - PDF/TXT           │─────▶│ - Duration       │
│ - Paste Text        │      │ - Start Date     │
└─────────────────────┘      └────────┬─────────┘
                                      │
                                      ▼
                              ┌───────────────┐
                              │ Click Generate│
                              └───────┬───────┘
                                      │
                                      ▼
                          ┌─────────────────────┐
                          │  AI Processing      │
                          │  Groq Llama 3.3 70B │
                          └──────────┬──────────┘
                                     │
                                     ▼
                    ┌────────────────────────────────┐
                    │  Create Study Schedule         │
                    │  - Weekly Topics               │
                    │  - Daily Objectives            │
                    │  - Study Hours                 │
                    └────────────┬───────────────────┘
                                 │
                                 ▼
                    ┌────────────────────────────────┐
                    │  Add Resources                 │
                    │  - YouTube Videos              │
                    │  - Quiz Questions              │
                    └────────────┬───────────────────┘
                                 │
                                 ▼
                    ┌────────────────────────────────┐
                    │  Display Interactive Schedule  │
                    └────────────┬───────────────────┘
                                 │
                                 ▼
                    ┌────────────────────────────────┐
                    │  User Features                 │
                    │  - Take Quizzes                │
                    │  - Watch Videos                │
                    │  - Track Progress              │
                    │  - Export Calendar             │
                    └────────────────────────────────┘
```

---

## 🛠️ Tech Stack

### Backend
- **Flask** - Python web framework
- **Groq API** - AI inference (Llama 3.3 70B)
- **PyPDF2** - PDF text extraction
- **python-dotenv** - Environment variable management
- **Gunicorn** - Production WSGI server

### Frontend
- **Vanilla JavaScript** - No framework bloat
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with gradients
- **Font Awesome** - Icons

### Deployment
- **Railway** - Hosting platform
- **Nixpacks** - Build system
- **Docker** - Containerization support

### APIs & Services
- **Groq API** - Fast LLM inference
- **YouTube Search** - Video resource integration
- **iCalendar** - Calendar export format

---

## 🚂 Deployment on Railway

The app is deployed at: **[calhacks2025-learnitai.up.railway.app](https://calhacks2025-learnitai.up.railway.app)**

### Deploy Your Own

1. **Fork this repository**

2. **Create Railway account**
   - Go to [railway.app](https://railway.app)
   - Sign up for free

3. **Create new project**
   - Click "New Project"
   - Select "Deploy from GitHub repo"
   - Choose your forked repository

4. **Add environment variables**
   - Go to project settings
   - Add variable: `GROQ_API_KEY=your_key_here`

5. **Deploy!**
   - Railway will automatically build and deploy
   - Your app will be live at `your-app.up.railway.app`

### Custom Domain (Optional)
- Go to Settings → Domains
- Add your custom domain
- Update DNS records as shown

---

## 📝 Key Files Explained

```
CalHacks2025/
├── app.py                 # Flask backend API
├── requirements.txt       # Python dependencies
├── Dockerfile            # Docker configuration
├── railway.json          # Railway deployment config
├── nixpacks.toml         # Nixpacks build config
├── Procfile              # Process configuration
├── .env.example          # Environment template
├── static/
│   ├── app.js           # Frontend JavaScript logic
│   └── styles.css       # Responsive styling
└── templates/
    └── index.html       # Main HTML template
```

---

## 🎯 Use Cases

### For Students
- **First-Generation Students** - Structured learning path
- **Self-Learners** - Organize independent study
- **Online Courses** - Break down MOOC syllabi
- **Exam Prep** - Systematic review schedules

### For Educators
- **Course Planning** - Visualize syllabus pacing
- **Student Sharing** - Distribute study guides
- **Tutoring** - Create structured learning plans

---

## 💡 Future Enhancements

### Planned Features
- 🤝 **Collaborative Study Groups** - Study with classmates
- 💬 **AI Tutoring Chatbot** - Get help on specific topics
- 🎮 **Study Streak Gamification** - Maintain daily streaks
- ⚙️ **Custom Intensity Levels** - Light, moderate, intense study
- 🗃️ **Flashcard Generation** - Auto-create flashcards
- 📱 **Mobile App** - Native iOS/Android apps
- 🔗 **LMS Integration** - Canvas, Blackboard, Moodle
- 📧 **Email Reminders** - Daily study notifications
- 🎨 **Theme Customization** - Personalize your interface

---

## 🐛 Troubleshooting

### PDF Extraction Issues
**Problem:** PDF content not extracting properly  
**Solutions:**
- Ensure PDF contains selectable text (not scanned images)
- Try copy-pasting text manually into the text area
- Use a PDF with actual text layers

### API Errors
**Problem:** "API Error: 401" or "No API key"  
**Solutions:**
- Verify your Groq API key is correct
- Check that key is in `.env` file or added via web interface
- Ensure no extra spaces in the key
- Try generating a new API key

### Schedule Not Generating
**Problem:** Loading spinner runs forever  
**Solutions:**
- Provide detailed syllabus content (more than just topic names)
- Check browser console for errors (F12)
- Try a shorter duration first (4-8 weeks)
- Verify internet connection
- Check API quota hasn't been exceeded

### Browser Compatibility
**Problem:** Features not working  
**Solutions:**
- Use a modern browser (Chrome, Firefox, Safari, Edge)
- Enable JavaScript
- Clear browser cache
- Try incognito/private mode

### Progress Not Saving
**Problem:** Completion marks disappear  
**Solutions:**
- Enable browser local storage
- Don't use private/incognito mode
- Check browser storage settings

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Report Bugs
- Use GitHub Issues
- Provide detailed description
- Include screenshots if applicable
- Share browser console errors

### Suggest Features
- Open a GitHub Issue
- Describe the feature
- Explain the use case
- Discuss implementation ideas

### Submit Pull Requests
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see below for details.

```
MIT License

Copyright (c) 2025 Sahil Dadhwal, Vicky Kang, Mai Westfall

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🏆 Hackathon Features

Perfect for CalHacks 2025 because:

- ✅ **Solves Real Problem** - Addresses 33% dropout rate
- ✅ **Cutting-Edge AI** - Uses Groq's fastest inference
- ✅ **Beautiful UI** - Modern, responsive design
- ✅ **Practical & Useful** - Students can use immediately
- ✅ **Easy to Demo** - Quick setup and clear value prop
- ✅ **Scalable Concept** - Can grow into full platform
- ✅ **Social Impact** - Helps underserved students succeed

---

## 📧 Contact & Team

**Project Repository:** [github.com/sahildadhwal/CalHacks2025](https://github.com/sahildadhwal/CalHacks2025)  
**Live Demo:** [calhacks2025-learnitai.up.railway.app](https://calhacks2025-learnitai.up.railway.app)

**Team Members:**
- **Sahil Dadhwal** - Full Stack Development
- **Vicky Kang** - AI Integration & Backend
- **Mai Westfall** - UI/UX Design & Frontend

**Built for:** CalHacks 2025  
**Built with:** ❤️ and lots of ☕

---

## 🙏 Acknowledgments

- **Groq** - For providing fast, free AI inference
- **Cal Hacks** - For organizing an amazing hackathon
- **YouTube** - For educational content integration
- **Open Source Community** - For amazing tools and libraries

---

## 📊 Project Stats

- **Lines of Code:** ~2,500+
- **Development Time:** 36 hours (hackathon)
- **Technologies Used:** 10+
- **Coffee Consumed:** ∞
- **Students Helped:** Growing!

---

**⭐ Star this repo if you find it helpful!**

**🚀 Good luck with your studies, and happy learning!**

---

*Made with passion during CalHacks 2025* 🎓✨