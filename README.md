# WriteSprint - Flutter AI-powered content writing trainer (scaffold)

This repository is a minimal scaffold for the WriteSprint Android app (Flutter). It implements:
- dynamic daily lesson fetching from an LLM (via an API service)
- local caching with Hive for offline use
- simple UI: Home, Lesson, Exercise screens
- basic progress tracking (XP, streak) via SharedPreferences

IMPORTANT: This is a scaffold. You must perform additional local setup:
1. Install Flutter SDK and tools.
2. Run `flutter pub get`.
3. Add a `.env` file in the project root (do NOT commit). Example:
```
OPENAI_API_KEY=sk-xxx
OPENAI_ENDPOINT=https://api.openai.com/v1/chat/completions
OPENAI_MODEL=gpt-4o-mini
```
4. Generate Hive adapters:
```
flutter pub run build_runner build
```
5. Run the app:
```
flutter run
```

Security note:
- Do NOT ship your API key inside the app. Use a backend/cloud function to proxy requests in production.

Files included:
- `pubspec.yaml`
- `lib/` with main.dart, models, services, and screens
- `.gitignore`

If you want, I can also generate a Cloud Function (Node.js) to proxy LLM requests. 
