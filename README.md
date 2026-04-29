 
🥗 CalTrack Food Database

A structured, scalable JSON-based food dataset designed for calorie tracking applications.
This repository powers the CalTrack mobile app with reliable nutritional data.

⸻

🚀 Overview

This dataset contains commonly used global and regional foods with:

* Calories (kcal)
* Macronutrients (Protein, Carbs, Fat)
* Micronutrients (Cholesterol, Sodium, Calcium, Iron, Potassium)
* Default serving sizes
* Search-friendly terms

The data is optimized for:

* 📱 Mobile apps (React Native, Flutter)
* ⚡ Fast search and filtering
* 🌐 Offline-first architecture
* 🔄 Version-based updates

⸻

📦 JSON Structure

{
  "version": 2,
  "foods": [
    {
      "id": "food_rice_white",
      "name": "White Rice (Boiled)",
      "category": "carbs",
      "emoji": "🍚",
      "base": { "unit": "g", "qty": 100 },
      "nutrition": {
        "calories": 130,
        "protein": 2.4,
        "carbs": 28.2,
        "fat": 0.3
      },
      "micros": {
        "cholesterol": 0,
        "sodium": 1,
        "calcium": 10,
        "iron": 0.2,
        "potassium": 35
      },
      "default_serving": {
        "name": "1 bowl",
        "grams": 150
      },
      "regions": ["global"],
      "tags": ["veg", "grain"],
      "searchTerms": ["rice", "white rice"],
      "is_verified": true,
      "updatedAt": "2026-04-27"
    }
  ]
}

⸻

🔄 Versioning System

The dataset uses a version-based update system:

* version increases when data changes
* Apps compare local version with remote version
* If updated → merge new data into local database

⸻

⚡ How It Works in App

App Start
   ↓
Fetch JSON from URL
   ↓
Compare version
   ↓
If updated → merge into local DB
   ↓
Use DB for fast access

⸻

🧠 Key Features

* ✅ Unique IDs (no duplicates)
* ✅ Per 100g standardized nutrition
* ✅ Dynamic serving calculations
* ✅ Lightweight and fast
* ✅ Easy to scale (100 → 10,000 foods)

⸻

⚠️ Important Notes

* Nutrition values are approximate and may vary slightly
* Do not rely on this dataset for medical purposes
* Always use id for data operations (not name)

⸻

🔮 Future Improvements

* Add more global foods
* Improve micronutrient coverage
* Add barcode support
* Add images for foods
* AI-assisted food expansion

⸻

🤝 Contributing

You can contribute by:

* Adding new foods
* Improving existing data
* Fixing incorrect values

⸻

📄 License

Free to use for personal and commercial projects.

⸻

💡 Powered By

Built for the CalTrack App – a modern calorie tracking solution.

⸻
