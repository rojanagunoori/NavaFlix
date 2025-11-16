 🎬 NavaFlix

# 🎬 NavaFlix

[![License: MIT](https://img.shields.io/badge/License-MIT-green)](https://opensource.org/licenses/MIT) 
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-blue)](https://nava-flix.vercel.app/)
[![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js)](https://nextjs.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.3-blue?logo=tailwind-css)](https://tailwindcss.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18-green?logo=node.js)](https://nodejs.org/)
[![GitHub stars](https://img.shields.io/github/stars/rojanagunoori/NavaFlix?style=social)](https://github.com/rojanagunoori/NavaFlix/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/rojanagunoori/NavaFlix?style=social)](https://github.com/rojanagunoori/NavaFlix/network)

NavaFlix is a **modern movie & TV discovery platform** built with **Next.js**, **TypeScript**, and **TailwindCSS**.  
It fetches **real-time data from TMDB API** and provides a smooth streaming-style experience with **watchlists, pagination, episode navigation, and AI-powered content descriptions**.  

🔗 **Live Demo:** [NavaFlix](https://nava-flix.vercel.app/)  
🔗 **GitHub Repo:** [NavaFlix GitHub](https://github.com/rojanagunoori/NavaFlix)

---

## 🚀 Features

- 🎬 Browse movies & TV shows: **trending, popular, top rated, now playing, upcoming**  
- 🔍 **Search:** Movies, TV shows, or actors  


NavaFlix is a **modern movie and TV discovery platform**, built with **Next.js**, **TypeScript**, and **TailwindCSS**.  
It fetches real-time data from **TMDB API** and provides a smooth, streaming-style experience with **watchlists, pagination, episode navigation, and AI-powered descriptions**.  

🔗 **Live Demo:** [NavaFlix](https://nava-flix.vercel.app/)  
🔗 **GitHub Repo:** [NavaFlix GitHub](https://github.com/rojanagunoori/NavaFlix)

---

## 🌟 Project Overview

NavaFlix allows users to:

- Browse movies & TV shows by **trending, popular, top rated, now playing, upcoming**
- View **movie & series details**, including overview, genres, cast, ratings
- Search for content in real-time
- Add content to a **personal watchlist**
- Navigate **seasons and episodes** for TV series
- View **AI-generated content descriptions** for fun facts and suggestions

This project uses **Next.js App Router**, **TailwindCSS**, **ShadCN UI**, and **Lucide icons** for a modern, accessible UI.

---

## 🚀 Features

- 🎬 Browse movies and TV shows by **trending, popular, top rated, now playing, upcoming**  
- 🔍 **Search**: Quickly find movies, TV shows, or actors  
- 🖼️ **High-quality posters and backdrops** via TMDB  
- 📜 **Watchlist**: Add/remove items with a single click  
- ⏭️ **Episode navigation**: Navigate through seasons & episodes of TV shows  
- 📱 Fully **responsive and mobile-first**  
- 🧩 **Custom pagination** with ellipsis for large lists  
- 💡 Optional **AI summaries** (via Gemini API) for enhanced content descriptions  
- 🎨 Dark & light theme support  

---

## 🏗️ Tech Stack

- **Framework:** Next.js 14 (App Router)  
- **Language:** TypeScript  
- **Styling:** TailwindCSS, ShadCN UI  
- **Icons:** Lucide Icons  
- **API:** TMDB REST API, Gemini API  
- **State Management:** Local state and watchlist hooks  
- **Deployment:** Vercel  

---

## 📁 Project Structure
```bash
NavaFlix/
├── app/                                # Next.js App Router
│   ├── api/                            # API Routes
│   │   ├── ai-facts/                   # AI facts API
│   │   │   └── route.ts
│   │   ├── ai-suggestions/             # AI suggestions API
│   │   │   └── route.ts
│   │   └── genres/                     # Genres API
│   │       └── route.ts
│   │
│   ├── movie/                          # Movie pages
│   │   └── [id]/page.tsx               # Movie details
│   │
│   ├── series/                         # TV series pages
│   │   └── [id]/page.tsx               # Series details
│   │
│   ├── search/page.tsx                 # Search page
│   ├── watchlist/page.tsx              # Watchlist page
│   ├── favicon.ico
│   ├── globals.css                     # Global styles
│   ├── layout.tsx                      # Root layout
│   ├── not-found.tsx                   # 404 page
│   └── page.tsx                        # Home page
│
├── components/                          # Reusable components
│   ├── display/                         # Media display components
│   │   ├── ImageCard.tsx
│   │   ├── MediaCard.tsx
│   │   ├── MediaPlayer.tsx
│   │   └── MediaPoster.tsx
│   │
│   ├── filter/                          # Filters for media
│   │   ├── Filter.tsx
│   │   ├── FilterWrapper.tsx
│   │   └── MediaFilter.tsx
│   │
│   ├── footer/                          # Footer component
│   │   └── Footer.tsx
│   │
│   ├── hero/                            # Homepage hero section
│   │   └── Hero.tsx
│   │
│   ├── info/                            # Info & metadata sections
│   │   ├── CategorySection.tsx
│   │   ├── DidYouKnowSection.tsx
│   │   └── MediaMeta.tsx
│   │
│   ├── layout/                          # Layout helpers
│   │   ├── MediaDetailLayout.tsx
│   │   ├── PaginationWrapper.tsx
│   │   ├── ResponsiveGrid.tsx
│   │   └── SectionHeader.tsx
│   │
│   ├── loading/                         # Loading indicators
│   │   ├── EpisodeLoading.tsx
│   │   └── PageLoading.tsx
│   │
│   ├── movie/                           # Movie-specific components
│   │   ├── MovieDisplay.tsx
│   │   ├── MovieInfo.tsx
│   │   └── MoviePageClient.tsx
│   │
│   ├── navbar/                          # Navigation & header
│   │   ├── AiSuggestionLink.tsx
│   │   ├── Header.tsx
│   │   ├── Logo.tsx
│   │   └── MobileMenu.tsx
│   │
│   ├── not-found/                       # 404 / missing content
│   │   ├── EpisodeNotFound.tsx
│   │   ├── InfoNotFound.tsx
│   │   └── SeasonNotFound.tsx
│   │
│   ├── pagination/                      # Pagination & navigation
│   │   ├── EpisodeNavigation.tsx
│   │   ├── GenericPagination.tsx
│   │   └── NextEpisode.tsx
│   │
│   ├── search/                          # Search components
│   │   ├── SearchBar.tsx
│   │   ├── SearchDisplay.tsx
│   │   └── SearchPageContent.tsx
│   │
│   ├── series/                          # TV series components
│   │   ├── EpisodeCard.tsx
│   │   ├── EpisodeDisplay.tsx
│   │   ├── EpisodeInfo.tsx
│   │   ├── EpisodeMeta.tsx
│   │   ├── SeasonCard.tsx
│   │   ├── SeasonDetails.tsx
│   │   ├── SeasonDisplay.tsx
│   │   ├── SeasonInfo.tsx
│   │   ├── SeriesPageClient.tsx
│   │   ├── TvDetails.tsx
│   │   ├── TvDisplay.tsx
│   │   └── TvInfo.tsx
│   │
│   ├── suggestions/                     # AI suggestions modal
│   │   └── AISuggestionModal.tsx
│   │
│   ├── title/                           # Page titles
│   │   └── PageTitle.tsx
│   │
│   ├── ui/                              # UI primitives
│   │   ├── button.tsx
│   │   ├── dialog.tsx
│   │   ├── label.tsx
│   │   ├── pagination.tsx
│   │   ├── RefreshButton.tsx
│   │   └── select.tsx
│   │
│   └── watchlist/                        # Watchlist components
│       ├── WatchlistButton.tsx
│       └── WatchListClient.tsx
│
├── lib/                                 # API, hooks, utils, types
│   ├── api.ts
│   ├── geminiService.ts
│   ├── hooks.ts
│   ├── logger.ts
│   ├── types.ts
│   ├── useAIFacts.ts
│   ├── useResume.ts
│   ├── useWatchlist.ts
│   └── utils.ts
│
├── .env.local                            # Environment variables (API keys)
├── README.md                             # Project documentation


```

---

## 🔑 Environment Variables

Create a `.env.local` file:

```bash
TMDB_API_KEY=your_tmdb_api_key
TMDB_API_BASE1=https://api.themoviedb.org/3
TMDB_IMAGE_BASE1=https://image.tmdb.org/t/p


# API Keys (server-side only)
TMDB_ACCESS_TOKEN=your_tmdb_api_key
GEMINI_API_KEY=your_gemini_api_key
# Environment
NODE_ENV=development
FORCE_CONSOLE_LOGGING=true
DEBUG_LOGGING=true

# Logging configuration
LOG_SERVICE_TIMEOUT_MS=3000
LOG_MAX_SIZE=10M
LOG_ROTATION_INTERVAL=1d
LOG_MAX_FILES=14
LOG_COMPRESS=true
LOG_FILE_PATH=logs/app.log
LOG_SERVICE_URL=https://logs.service.com/api # ,https://your-log-service.example.com

# Allowed origins (comma separated)
ALLOWED_ORIGINS=http://localhost:3000 #,https://yourdomain.com

# Client-side keys (must start with NEXT_PUBLIC_)
NEXT_PUBLIC_TMDB_API_KEY=your_public_tmdb_key
NEXT_PUBLIC_GEMINI_API_KEY=your_public_gemini_key
```
### ⚡ Installation
Clone the repo:
```bash
git clone https://github.com/rojanagunoori/NavaFlix.git
cd NavaFlix
npm install
```
### Run locally:

```bash
npm run dev
```
Open your browser at http://localhost:3000

## 🛠️ Build for Production
```bash
npm run build
npm start
```
## 🔌 API Usage
### Fetch Trending Movies Example:

```bash
export const fetchTrendingMovies = async () => {
  const res = await fetch(
    `${process.env.TMDB_API_BASE1}/trending/movie/day?api_key=${process.env.TMDB_API_KEY}`
  );
  return res.json();
};
```
### Fetch TV Episode Details Example:

```bash
export const getEpisodeDetails = async (seriesId, season, episode) => {
  return fetch(
    `${process.env.TMDB_API_BASE1}/tv/${seriesId}/season/${season}/episode/${episode}?api_key=${process.env.TMDB_API_KEY}`
  ).then(res => res.json());
};
```
### Generate AI Content Summary (Gemini API)

```bash
import { generateSummary } from '../lib/geminiService';

const summary = await generateSummary({
  prompt: "Write a short AI-powered summary for the movie 'Inception'.",
  maxTokens: 150
});

console.log(summary);
```
#### Example Gemini Service (lib/geminiService.ts):

```bash
export const generateSummary = async ({ prompt, maxTokens = 150 }: { prompt: string; maxTokens?: number }) => {
  const res = await fetch('https://api.gemini.com/v1/ai/summarize', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      'Authorization': `Bearer ${process.env.GEMINI_API_KEY}`
    },
    body: JSON.stringify({ prompt, maxTokens })
  });

  const data = await res.json();
  return data.text;
};
```
💡 The Gemini API can generate AI summaries, recommendations, or fun facts for movies and TV shows.

## 🧩 Key Components

### 🎬 Media Display
- **🃏 MediaCard** – Displays a movie or TV show with poster, title, rating, and release date.  
- **🖼️ MediaPoster** – Renders only the poster image for movies or TV shows.  
- **▶️ MediaPlayer** – Video player for trailers or full content previews.  
- **🖼️ ImageCard** – Generic card for images, used in hero sections or suggestions.  

### 🎥 Movie Components
- **🎞️ MovieDisplay** – Shows detailed movie info (overview, genres, ratings).  
- **ℹ️ MovieInfo** – Renders movie metadata such as release date, runtime, and language.  
- **💻 MoviePageClient** – Client-side wrapper to handle dynamic movie content.  

### 📺 Series Components
- **📺 TvDisplay** – TV show details including seasons and episodes.  
- **ℹ️ TvInfo** – TV metadata like first air date, language, and origin country.  
- **💻 SeriesPageClient** – Client-side wrapper for series details.  
- **📅 SeasonDisplay / SeasonInfo / SeasonDetails** – Displays season-specific info.  
- **🎬 EpisodeDisplay / EpisodeInfo / EpisodeCard / EpisodeMeta** – Episode metadata and playback navigation.  
- **⏭️ EpisodeNavigation** – Navigate between episodes and seasons.  
- **➡️ NextEpisode** – Quick access to the next episode in a series.  

### ⭐ Watchlist
- **➕ WatchlistButton** – Add/remove movies or TV shows to/from the watchlist.  
- **📋 WatchListClient** – Displays user’s watchlist with all items.  

### 🔍 Search & Filter
- **🔎 SearchBar** – Input field for searching movies, series, or actors.  
- **🗂️ SearchDisplay / SearchPageContent** – Shows search results in a grid.  
- **⚙️ Filter / FilterWrapper / MediaFilter** – Filters media by genre, rating, or type.  

### 🧭 Navigation & Layout
- **🧩 Header / Logo / MobileMenu** – Navbar, branding, and responsive menu.  
- **📄 PaginationWrapper / GenericPagination** – Custom pagination with ellipsis support.  
- **🔲 ResponsiveGrid** – Grid layout for media cards and sections.  
- **🏷️ SectionHeader** – Section title with styling.  
- **📐 MediaDetailLayout** – Layout wrapper for movie/series detail pages.  

### 🖌️ UI Primitives
- **🔘 Button** – Reusable button with variants and sizes.  
- **🗔 Dialog** – Modal dialog with header, footer, and close functionality.  
- **🏷️ Label** – Styled label for forms or UI.  
- **🔄 RefreshButton** – Reloads the current page.  
- **🔽 Select** – Custom dropdown/select component.  
- **📄 Pagination** – Navigation buttons for pages with active state.  

### 🌟 Hero & Info Sections
- **🏆 Hero** – Homepage hero section with featured content.  
- **📚 CategorySection** – Displays movies/series by categories like trending or top-rated.  
- **💡 DidYouKnowSection** – Fun facts powered by AI.  
- **ℹ️ MediaMeta** – Shows ratings, runtime, genres, and other metadata.  

### 🤖 AI & Suggestions
- **💡 AISuggestionModal** – Shows AI-powered suggestions for media based on user interest.  
- **🔗 AiSuggestionLink** – Quick link to open AI suggestions.  

### ❌ Not Found / ⏳ Loading
- **⏳ PageLoading / EpisodeLoading** – Loading spinners and placeholders.  
- **❌ InfoNotFound / EpisodeNotFound / SeasonNotFound** – 404 or missing content displays.  

💡 **Tip:** Include screenshots of each component to make the README visually appealing and easier to understand.

## 🤝 Contributing
1. Fork the repository

2. Create a branch: `git checkout -b feature/YourFeature`

3. Commit changes: `git commit -m 'Add some feature'`

4. Push to branch: `git push origin feature/YourFeature`

5. Create a Pull Request

## 📄 License
This project is licensed under the MIT License.

## 👨‍💻 Author
Roja nagunoori
Full Stack Developer | [GitHub](https://github.com/rojanagunoori/NavaFlix.git)

🌐 Live Demo
Check the live app at https://nava-flix.vercel.app/

