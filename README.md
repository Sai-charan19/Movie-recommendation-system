# MovieMind AI

An intelligent movie discovery platform powered by AI that learns from your searches and preferences.

## 🎬 Features

### Multi-Language Support
- **13 Languages**: English, Hindi, Tamil, Telugu, Korean, Japanese, Spanish, French, Portuguese, Chinese, German, Italian, and Russian
- **45+ Movies**: Curated collection from around the world including Parasite, RRR, Vikram, Spirited Away, City of God, and more
- **Language Filter**: Quick dropdown to filter movies by language with flag icons

### AI-Powered Features

#### 🧠 Smart Search Learning
- Search for any movie not in the database
- AI detects zero results and waits ~1.8 seconds
- Automatically creates a movie card with inferred language and genre
- Saves to localStorage - appears permanently on next visit
- Displays "AI Generated" badge on learned movies

#### 🤖 AI Chatbot
- Floating red button in bottom-right corner
- Natural language queries:
  - "suggest Korean thrillers"
  - "recommend based on my favorites"
  - "I want something scary"
  - Type any movie name directly
- Returns curated picks you can click to open details
- Contextual responses based on your watch history and favorites

#### ✨ AI Recommendations Sidebar (Desktop)
- **Personalized Picks**: Based on your top genre from favorites
- **AI Just Learned**: Shows recently searched movies
- **Trending Now**: High-rated recent releases
- **Your Stats**: Movies watched, favorite genre, AI learned count

### Core Features

- **Favorites System**: Heart button to save favorites with localStorage persistence
- **Watch History**: Eye button to mark as watched, separate "Watched" tab
- **Movie Details Modal**: 
  - Full-screen backdrop with poster overlay
  - Complete overview, genres, ratings
  - Year, language, and rating display
  - Favorite & watched toggle buttons
- **Smart Filters**:
  - Genre filter bar (Action, Drama, Sci-Fi, etc.)
  - Language selector dropdown
  - Sort options (Rating / Newest / A-Z)
  - Real-time search by title/keyword
- **Responsive Grid**: Adapts from 5 columns on desktop to 2 on mobile

## 🎨 Design

- **Dark Cinema Aesthetic**: Deep near-black background (#09090b zinc-950)
- **Crimson Red Accents**: Primary color for buttons and highlights
- **Barlow Condensed**: Display typeface for headings (cinematic feel)
- **Inter**: Body text for readability
- **Smooth Animations**: Hover effects, scale transforms, and transitions

## 🤖 How AI Learning Works

1. User searches for "Bahubali" (not in database)
2. AI detects 0 search results
3. After 1.8s, AI infers:
   - Language: Hindi (from title keywords)
   - Genre: Action/Drama (default inference)
   - Year: 2024 (current)
   - Rating: 7.5 (placeholder)
4. Creates movie card with "AI ✨" badge
5. Saves to localStorage under `moviemind-ai-movies`
6. Next visit: Movie appears in grid permanently

## 💾 LocalStorage Keys

- `moviemind-favorites`: Array of favorite movie IDs
- `moviemind-watched`: Array of watched movie IDs
- `moviemind-ai-learned`: Array of AI learned movie metadata
- `moviemind-ai-movies`: Full movie objects for AI-generated entries

## 🚀 Tech Stack

- React 18 + TypeScript
- Tailwind CSS v4
- Lucide React (icons)
- localStorage for persistence
- Custom AI inference logic

## 📱 Responsive Breakpoints

- Mobile: 2 columns (base)
- Tablet: 3 columns (md)
- Desktop: 4 columns (lg)
- Large Desktop: 5 columns (xl)
- AI Sidebar: Hidden below xl breakpoint

## 🎯 Future Enhancements

- Connect to real movie API (TMDB, OMDb)
- Enhanced AI learning with genre/language confidence scores
- User accounts and cloud sync
- Advanced recommendation algorithms
- Movie trailers and streaming availability
- Social features (reviews, ratings)
