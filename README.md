NewsMag - React News Application
A modern, responsive news application built with React that fetches and displays the latest news articles from various categories using the NewsAPI.
Features

📰 Real-time news updates from NewsAPI
🎯 Multiple news categories (Technology, Business, Health, Science, Sports, Entertainment)
🎨 Dark-themed UI using Bootstrap
📱 Fully responsive design
🖼️ Fallback images for articles without thumbnails
🔄 Dynamic category switching
![NewsMag App](/newsapp.png)
Tech Stack

React (v18+) - Frontend framework
Vite - Build tool and development server
Bootstrap 5 - UI framework for styling
NewsAPI - News data provider

Prerequisites
Before you begin, ensure you have the following installed:

Node.js (v14 or higher)
npm or yarn package manager
A NewsAPI key (get it free at newsapi.org)

Installation
Clone the repository
git clone <your-repository-url>
cd news

Set up environment variables
Create a .env file in the root directory:
VITE_API_KEY=your_newsapi_key_here

Run the development server
npm run dev

Open your browser
Navigate to http://localhost:5173 (or the port shown in your terminal)

 Usage
Browsing News

Click on any category in the navigation bar to filter news by topic
Each news card displays:

Article image (or fallback image if unavailable)
Title (truncated to 50 characters)
Description (truncated to 90 characters)
"Read More" button linking to the full article



Available Categories

General (default)
Technology
Business
Health
Science
Sports
Entertainment

API Configuration
This app uses NewsAPI to fetch news articles. The API call is configured in NewsBoard.jsx:
javascriptlet url = `https://newsapi.org/v2/top-headlines?country=us&category=${category}&apiKey=${import.meta.env.VITE_API_KEY}`
Note on API Limits

NewsAPI free tier allows 100 requests per day
Articles are limited to those from the United States (country=us)

Customization
Change Country
Edit the URL in NewsBoard.jsx:
javascript// Change 'us' to your desired country code (e.g., 'in', 'gb', 'ca')
let url = `https://newsapi.org/v2/top-headlines?country=in&category=${category}&apiKey=...`
Modify Categories
Edit the navigation items in NavBar.jsx to add or remove categories.
Styling

Bootstrap classes are used throughout for styling
Custom styles can be added to App.css or index.css
The app uses a dark theme (data-bs-theme="dark")

Known Issues

Typo in NavBar.jsx: "Busniness" should be "Business" (line 19)
NewsAPI free tier has limited daily requests
Some articles may not have images or descriptions

Contributing

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

License
This project is open source and available under the MIT License.
Acknowledgments

NewsAPI for providing the news data
Bootstrap for the UI components
Vite for the blazing fast build tool

Contact
For questions or support, please open an issue in the repository.

Happy Reading! 📰
