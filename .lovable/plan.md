
# AI Job Recommendation System

## Overview
A full-stack job recommendation platform that matches users to jobs based on their skills, experience, and preferences using TF-IDF/Cosine Similarity algorithm - all powered by Lovable Cloud.

---

## Pages & Features

### 1. **Home Page**
- Clean hero section introducing the app
- "Find Your Perfect Job Match" headline
- Call-to-action button to start the job matching process
- Brief explanation of how the matching works

### 2. **Job Finder Form Page**
- Multi-step or single-page form with:
  - **Skills input**: Multi-select with auto-suggest from common skills (React, Python, SQL, etc.)
  - **Years of experience**: Dropdown or slider (0-1, 1-3, 3-5, 5+)
  - **Preferred role**: Select from categories (Data Analyst, Developer, Designer, etc.)
  - **Location preference**: Text input or select (Remote, specific cities)
- Form validation with helpful error messages
- Loading animation while processing

### 3. **Results Page**
- List of matched jobs ranked by relevance
- Each job card shows:
  - Job title
  - Company name
  - Required skills (with highlights for matching skills)
  - Experience level required
  - **Match percentage** (e.g., 92% match)
  - "Apply" button (links to job posting)
- Filter/sort options (by match %, experience level)
- "Try Again" button to refine search

### 4. **Admin Panel** (Optional bonus)
- Simple interface to add/edit/delete jobs in the database
- Password protected access

---

## Backend & Database (Lovable Cloud)

### Database Tables
- **jobs**: Stores job listings with title, company, required skills, experience level, location, apply URL
- **skills**: Master list of skills for auto-suggest

### Edge Function
- **recommend-jobs**: Receives user input, runs TF-IDF/cosine similarity matching, returns ranked job list with match percentages

---

## Matching Algorithm
- **TF-IDF Vectorization**: Convert user skills and job requirements into numerical vectors
- **Cosine Similarity**: Calculate similarity score between user profile and each job
- **Ranking**: Return jobs sorted by match percentage
- Built entirely in TypeScript - no external AI APIs needed

---

## Design
- Clean, modern UI with Tailwind CSS
- Responsive for mobile and desktop
- Professional color scheme (blues/greens for trust)
- Smooth animations and transitions
- Clear visual hierarchy

---

## Sample Flow
1. User enters: Python, Machine Learning, SQL | 1 year | Data Analyst | Remote
2. System calculates similarity with all jobs
3. Results display:
   - Junior Data Analyst – 92% match ✓
   - ML Intern – 87% match
   - Business Analyst – 79% match
