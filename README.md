# calorieCounter - Frontend
This website is for fitness and nutrition people to keep track of their daily calorie intake

## 📱 Android APK Download

A native Android app is also available. You can download the latest APK directly:

- **[Download APK](https://github.com/JavaByMohamed/calorieCounterAndroid/releases/latest/download/app-release.apk)** — Install on any Android device
- **[View All Releases](https://github.com/JavaByMohamed/calorieCounterAndroid/releases)** — Browse release history

> **Note:** You may need to allow installs from unknown sources in your Android settings.

## Project Structure

calorieCounter/
│
├── index.html                // Main landing page
├── bmi-bmr.html              // BMI and BMR calculator page
├── meal.html                 // Add a meal and meal summary page
├── ingredients.html          // Manage ingredients page
├── styles.css                // Shared styles
├── script/
│   ├── mockDatabase.js       // Contains the mock nutrition database
│   ├── ingredientManagement.js // Manages ingredients (add, edit, delete)
│   ├── mealForm.js           // Handles meal form submission and display
│   ├── bmiBmr.js             // Handles BMI and BMR calculations
│   ├── dropdownMenu.js       // Handles the dropdown menu functionality
│   └── main.js               // Initializes the app and imports other scripts

## GitHub Pages proxy setup

When deployed to GitHub Pages, local `http://localhost:8081` proxy calls will not work.

1. Deploy your proxy (see `fatsecret-proxy/README.md`).
2. Open `script/runtimeConfig.js`.
3. Set:

```javascript
window.CALORIE_COUNTER_PROXY_URL = "https://your-proxy-name.workers.dev";
```

If left empty, the app uses localhost during local development and falls back to Open Food Facts for store search in production.

