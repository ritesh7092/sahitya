# 📚 Sahitya - AI Hindi Book Recommender

An intelligent recommendation system for Hindi literature built with machine learning and personalized user profiling. Sahitya discovers book recommendations tailored to individual user preferences through collaborative filtering and content-based recommendation algorithms.

## ✨ Features

- **User Authentication**: Secure login and registration system with hashed passwords
- **Cold Start Recommendations**: Intelligent initial recommendations based on popularity and ratings
- **Personalized Recommendations**: AI-driven suggestions that evolve with user interactions
- **User Profiling**: Automatically builds user preference profiles based on interaction history
- **Interactive Dashboard**: Streamlit-powered web interface for seamless user experience
- **Hindi Literature Focus**: Curated collection of classic and contemporary Hindi books, poetry, and literary works
- **Data Visualization**: Visual insights into recommendation scores and user preferences

## 🎯 How It Works

### Cold Start Phase
New users receive recommendations based on popularity scores and overall ratings, ensuring they get quality content immediately.

### Personalized Phase
As users interact with recommendations (clicks, selections), the system:
1. Tracks user interactions
2. Builds a preference profile from clicked items
3. Extracts preferred tags and categories
4. Generates personalized recommendations matching user interests

## 🛠️ Technology Stack

- **Backend**: Python
- **Frontend**: Streamlit (Interactive web interface)
- **Machine Learning**: scikit-learn
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Authentication**: SHA-256 password hashing
- **Data Storage**: CSV (products, users) and JSON (user profiles)

## 📋 Requirements

```
streamlit
pandas
numpy
matplotlib
scikit-learn
Pillow
seaborn
```

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/ritesh7092/sahitya.git
   cd sahitya
   ```

2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Generate product data** (if products.csv doesn't exist)
   ```bash
   python generate_products.py
   ```

## 📊 Running the Application

### Launch the Web Application
```bash
streamlit run app.py
```
The application will open in your browser at `http://localhost:8501`

### Run Recommendation Demo
```bash
python recommend.py
```
This demonstrates the recommendation system with sample data and visualizations.

## 📁 Project Structure

```
sahitya/
├── app.py                    # Main Streamlit application
├── auth.py                   # Authentication & user management
├── recommend.py              # Recommendation system demo
├── utils.py                  # Core recommendation algorithms
├── visualize.py              # Data visualization functions
├── generate_products.py      # Product dataset generator
├── requirements.txt          # Python dependencies
├── products.csv              # Hindi books database
├── users.json                # User credentials storage
├── users.csv                 # User interaction history
├── data/
│   ├── products.csv          # Product data backup
│   ├── users.csv             # User data backup
│   ├── images/               # Book cover images
│   └── profiles/             # User preference profiles
└── __pycache__/              # Python cache files
```

## 🔐 Authentication

- Users can register with a username and password
- Passwords are securely hashed using SHA-256
- User credentials are stored in `users.json`
- Session management through Streamlit's session state

## 📚 Sample Data

The system includes a curated collection of Hindi literature:

- **गोदान** (Godaan) by प्रेमचंद - Classic novel about rural life
- **रश्मिरथी** (Rashmirathi) by रामधारी सिंह दिनकर - Epic poetry
- **मधुशाला** (Madhushala) by हरिवंश राय बच्चन - Philosophical poetry
- And more classic works...

Each book includes tags (authors, genres, themes) and popularity scores for intelligent recommendations.

## 🤖 Recommendation Algorithms

### Cold Start Strategy
Recommends top-rated and most popular books for new users with no interaction history.

### User Profile Building
Analyzes clicked/selected items to extract:
- **Preferred tags**: Genres, authors, and themes the user engages with
- **Preferred categories**: Types of literature (poetry, novel, anthology)

### Personalized Scoring
Matches user profiles against available content to generate personalized recommendations.

## 📈 Future Enhancements

- [ ] Collaborative filtering with user-user similarity
- [ ] Content-based filtering with TF-IDF
- [ ] Rating system for more accurate preferences
- [ ] Reading history and progress tracking
- [ ] Social sharing and recommendations
- [ ] Advanced NLP for content analysis
- [ ] Admin dashboard for product management
- [ ] Email notifications for new releases

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs and issues
- Suggest new features
- Submit pull requests
- Improve documentation

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💼 Author

**Ritesh** - [GitHub Profile](https://github.com/ritesh7092)

## 📧 Support

For questions, issues, or suggestions, please open an issue on the GitHub repository.

---

**Happy Reading! 📖** Explore the world of Hindi literature with personalized recommendations.
