# Movie Recommender System

A Streamlit web app that recommends movies based on user selection using content-based filtering.

## Features

- Select movies from a dropdown list
- Get 5 movie recommendations with posters
- Clean, responsive UI with movie posters

## Local Development

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the app:
   ```bash
   streamlit run app.py
   ```

## Deployment on Render

### Step 1: Prepare Your Repository
1. Create a GitHub repository
2. Push your code to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/your-repo-name.git
   git push -u origin main
   ```

### Step 2: Deploy on Render
1. Go to [Render.com](https://render.com) and sign up/login
2. Click "New +" and select "Web Service"
3. Connect your GitHub repository
4. Configure the service:
   - **Name**: movie-recommender-app
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `streamlit run app.py --server.port $PORT --server.headless true --server.runOnSave false`
5. Click "Create Web Service"

### Step 3: Environment Variables (Optional)
If you need to set environment variables (like API keys), you can add them in the Render dashboard under "Environment".

## Files Structure

```
├── app.py                 # Main Streamlit application
├── movie_dict.pkl         # Movie data (titles, IDs, etc.)
├── similarity.pkl         # Pre-computed similarity matrix
├── requirements.txt       # Python dependencies
├── .gitignore            # Files to ignore in git
└── README.md             # This file
```

## API Used

- TMDb API for movie posters (requires API key in the code)

## Note

Make sure your pickle files (`movie_dict.pkl` and `similarity.pkl`) are included in your repository for the app to work.