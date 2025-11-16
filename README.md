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

## ⚠️ Challenges Faced During Development

During the development of **NavaFlix**, several technical and design challenges were encountered. Below is a detailed breakdown:

---

### 1. 📊 Managing Multiple APIs
- **Problem:** Integrating TMDB API for movies/TV shows alongside Gemini API for AI-generated content required careful handling of API limits, authentication, and error handling.  
- **Impact:** Ensuring consistent data structure across different endpoints (movies vs TV shows) was tricky and could break components.  
- **Solution:** Implemented modular API service functions, error handling, and caching where needed to maintain smooth performance.  

---

### 2. 🔌 TMDB API Rate Limits and Data Handling
- **Problem:** TMDB enforces strict API rate limits. Multiple calls for trending, popular, top-rated, and detail pages could exceed limits.  
- **Impact:** Frequent calls could cause blocked requests or delayed responses.  
- **Solution:** Implemented caching with custom hooks (`useWatchlist`, `useResume`) and conditional fetching logic.  

---

### 3. 🎛️ State Management
- **Problem:** Features like watchlist required syncing between local state, `localStorage`, and dynamic components.  
- **Impact:** Incorrect updates could lead to inconsistent UI or require page reloads.  
- **Solution:** Built `useWatchlist` hook with proper synchronization. Components like `WatchlistButton` reflect real-time changes.  

---

### 4. ⏭️ Episode & Season Navigation
- **Problem:** Navigating TV series with variable seasons and episodes was complex.  
- **Impact:** Users could encounter broken navigation, missing episodes, or incomplete season data.  
- **Solution:** Created reusable components like `EpisodeNavigation`, `NextEpisode`, `SeasonDisplay`, and `EpisodeCard` to ensure seamless navigation.  

---

### 5. 🔍 Search Performance Optimization
- **Problem:** Real-time search for movies, TV shows, and actors could overwhelm the API.  
- **Impact:** Slow or unresponsive search experience.  
- **Solution:** Implemented input debouncing and incremental rendering in `SearchDisplay`.  

---

### 6. 💡 AI Integration
- **Problem:** Fetching AI-powered summaries from Gemini API introduces latency.  
- **Impact:** Users could see empty or broken UI if AI data fails or is slow.  
- **Solution:** Used `useAIFacts` and `AISuggestionModal` with loading placeholders and error handling.  

---

### 7. 🖼️ Media Poster & Aspect Ratio Handling
- **Problem:** TMDB images have varying sizes and aspect ratios.  
- **Impact:** Could break grids or crop images inconsistently.  
- **Solution:** Designed `MediaPoster`, `MediaCard`, and `ResponsiveGrid` components to maintain proper scaling and responsive layouts.  

---

### 8. ⚡ Performance & Loading
- **Problem:** Movie/TV pages require multiple API calls and large images.  
- **Impact:** Slower page loads, flickering, or blank screens.  
- **Solution:** Implemented lazy loading for images, optimized API calls, and used loading indicators like `PageLoading` and `EpisodeLoading`.  

---

### 9. 🎨 UI/UX Design
- **Problem:** Designing a mobile-first streaming layout with hero sections, watchlist overlays, and dynamic grids was challenging.  
- **Impact:** Maintaining proper scaling for posters, cards, and metadata on different screen sizes required meticulous CSS work.  
- **Solution:** TailwindCSS responsive classes and reusable components like `MediaCard`, `Pagination`, and `Dialog`.  

---

### 10. Custom Pagination Logic
- **Problem:** Handling large datasets like trending movies or top-rated lists.  
- **Impact:** Users could get lost in long lists.  
- **Solution:** `GenericPagination` and `PaginationWrapper` components with ellipsis, previous/next buttons, and active page highlighting.  

---

### 11. SEO & Metadata Management
- **Problem:** Each movie/TV page needed unique titles, descriptions, and OG metadata.  
- **Impact:** Poor SEO ranking and incorrect social sharing previews.  
- **Solution:** Dynamic metadata generated using TMDB API in `MediaMeta` and `layout.tsx`.  

---

### 12. 📱 Responsive Design
- **Problem:** Complex streaming layout needed to be fully responsive.  
- **Impact:** Grids, hero sections, and watchlist overlays could break on smaller devices.  
- **Solution:** Mobile-first design, TailwindCSS responsive utilities, and testing on multiple screen sizes.  

---

### 13. Cross-Browser Compatibility
- **Problem:** Components rendered differently across browsers.  
- **Impact:** Broken layouts, misaligned grids, and inconsistent fonts.  
- **Solution:** Extensive testing and minor CSS adjustments for Chrome, Firefox, Safari, and mobile browsers.  

---

### 14. Accessibility (a11y)
- **Problem:** Buttons, dialogs, and pagination needed keyboard and screen reader support.  
- **Impact:** Accessibility violations could prevent users with disabilities from using the app.  
- **Solution:** Used Radix UI primitives with proper ARIA attributes and focus management.  

---

### 15. Environment & API Key Management
- **Problem:** API keys for TMDB and Gemini needed to remain secure.  
- **Impact:** Exposing keys in frontend could allow unauthorized access.  
- **Solution:** Used `.env.local` for server-side secrets and `NEXT_PUBLIC_` for client-side keys.  

---

### 16. Deployment Challenges
- **Problem:** Deploying Next.js App Router project with dynamic routes on Vercel.  
- **Impact:** Incorrect builds could break routing or dynamic pages.  
- **Solution:** Configured environment variables correctly and tested builds before deployment.  

---

### 17. 🌗 Dark & Light Mode (Optional)
- **Problem:** Planning for themes required global state and consistent styling.  
- **Impact:** Not implemented yet; UI remains in default theme.  
- **Solution:** Can be added later using TailwindCSS dark mode configuration.  

---

💡 **Tip:** Documenting challenges helps future contributors understand technical decisions and potential pitfalls.

---

## 🌟 Future Improvements

While **NavaFlix** is fully functional, several enhancements are planned to improve user experience, performance, and feature richness:

---

### 1. 🌗 Dark & Light Mode
- **Goal:** Implement full theme toggling between dark and light modes.  
- **Benefit:** Enhances accessibility and user comfort for different lighting conditions.  
- **Implementation:** Use TailwindCSS dark mode configuration and store theme preference in localStorage or context.  

---

### 2. ⚡ Advanced AI Features
- **Goal:** Expand Gemini API integration to provide:  
  - Personalized movie/TV recommendations  
  - AI-generated reviews or summaries  
  - Trivia and fun facts per movie or episode  
- **Benefit:** Makes the platform smarter and more interactive.  

---

### 3. 📈 Improved Performance & Caching
- **Goal:** Implement server-side caching for frequently accessed API endpoints.  
- **Benefit:** Reduces API calls, improves page load speed, and avoids TMDB/Gemini rate limits.  

---

### 4. 🎥 Video Previews & Trailers
- **Goal:** Embed video trailers or previews for movies and TV shows.  
- **Benefit:** Provides richer media experience and helps users decide what to watch.  

---

### 5. 🏷️ Enhanced Search & Filtering
- **Goal:** Add multi-criteria filters: genre, year, rating, language, etc.  
- **Benefit:** Improves content discoverability and user satisfaction.  

---

### 6. 🔗 User Authentication & Profiles
- **Goal:** Add user login via OAuth or custom authentication.  
- **Benefit:** Allows saving watchlists in the cloud, tracking watched content, and personalized recommendations.  

---

### 7. 🌐 Multi-Language Support
- **Goal:** Internationalize the platform for multiple languages.  
- **Benefit:** Expands audience reach globally.  

---

### 8. 📊 Analytics & Insights
- **Goal:** Track trending content, user engagement, and AI suggestion interactions.  
- **Benefit:** Helps optimize UI/UX and content strategy.  

---

### 9. 🛠️ Progressive Web App (PWA)
- **Goal:** Make NavaFlix installable as a PWA for offline access and mobile experience.  
- **Benefit:** Users can watch content and manage watchlists without relying entirely on the browser.  

---

### 10. 💡 Accessibility Enhancements
- **Goal:** Improve keyboard navigation, screen reader support, and color contrast.  
- **Benefit:** Makes NavaFlix fully accessible to all users.  

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

## 🙏 Acknowledgements
- [TMDB API](https://www.themoviedb.org/) for movie & TV data
- [Next.js](https://nextjs.org/) for the React framework
- [TailwindCSS](https://tailwindcss.com/) for styling
- [ShadCN UI](https://ui.shadcn.com/) for UI components
- [Gemini API](https://example.com) for AI summaries


## 📄 License
This project is licensed under the MIT License.

## 👨‍💻 Author
Roja nagunoori
Full Stack Developer | [GitHub](https://github.com/rojanagunoori/NavaFlix.git)

🌐 Live Demo
Check the live app at https://nava-flix.vercel.app/

