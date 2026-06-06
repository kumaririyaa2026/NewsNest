# NewsNest 📰

A real-time Android news application built with **Kotlin**, **MVVM architecture**, **Retrofit**, and **Room Database**.

## Features

- 🔍 **Search** news by keyword
- 📂 **Category filtering** — General, Technology, Business, Sports, Health, Entertainment, Science
- 🔖 **Save articles offline** using Room Database
- 🗑️ **Swipe to delete** saved articles with Undo support
- 🌐 **WebView** to read full articles in-app
- 🔄 **Pull to refresh** for latest headlines
- ⚡ Clean **MVVM** architecture with LiveData and ViewModel

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Kotlin |
| Architecture | MVVM |
| Networking | Retrofit 2 + OkHttp |
| Database | Room (SQLite) |
| Image Loading | Glide |
| UI | Material Design 3, ViewBinding |
| Navigation | Jetpack Navigation Component |
| Async | Kotlin Coroutines |

## Screenshots

> Add screenshots here after running the app

## Setup

### 1. Get a free API key
- Go to [https://newsapi.org](https://newsapi.org) and sign up (free)
- Copy your API key

### 2. Add your API key
Open `app/build.gradle` and replace:
```
buildConfigField("String", "NEWS_API_KEY", "\"YOUR_API_KEY_HERE\"")
```
with your actual key:
```
buildConfigField("String", "NEWS_API_KEY", "\"abc123yourkey\"")
```

### 3. Build and Run
- Open in **Android Studio Hedgehog** or later
- Sync Gradle
- Run on emulator or physical device (Android 7.0+)

## Architecture

```
com.riya.newsnest
├── data/
│   ├── api/          # Retrofit API service & client
│   ├── ArticleDao    # Room DAO
│   └── NewsDatabase  # Room database
├── model/            # Data classes (Article, NewsResponse)
├── repository/       # NewsRepository (single source of truth)
├── viewmodel/        # NewsViewModel
├── ui/
│   ├── adapter/      # RecyclerView adapter
│   ├── fragment/     # Headlines & Saved fragments
│   ├── MainActivity
│   └── ArticleDetailActivity
└── utils/            # Extensions, Resource, NetworkUtils
```

## License
MIT License — free to use and modify.
