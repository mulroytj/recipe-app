Recipe Database
A shared recipe collection app powered by Supabase and React.
Features

📸 OCR Recipe Extraction - Upload photos of recipes to automatically extract text
🔍 Smart Search - Search by ingredients, recipe name, tags, or source
🏷️ Categories & Tags - Organize recipes with categories and custom tags
💬 Comments - Discuss recipes with friends
✏️ Edit & Delete - Full CRUD operations
📱 PWA Support - Install as an app on iPhone/Android
🤝 Real-time Sharing - Changes sync via Supabase

Tech Stack

Frontend: React (via CDN)
Styling: Tailwind CSS
Backend: Supabase (PostgreSQL)
Icons: Lucide Icons
Hosting: GitHub Pages

Installation on iPhone

Open the app URL in Safari
Tap the Share button
Select "Add to Home Screen"
Tap "Add"

Local Development
Simply open index.html in a web browser. No build step required!
Database Schema
The app uses a Supabase PostgreSQL database with the following schema:
sqlCREATE TABLE recipes (
  id BIGINT PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
  name TEXT NOT NULL,
  ingredients JSONB NOT NULL,
  instructions TEXT,
  prep_time TEXT,
  servings TEXT,
  category TEXT NOT NULL,
  source TEXT,
  tags JSONB,
  added_by TEXT NOT NULL,
  date_added TIMESTAMPTZ DEFAULT NOW(),
  last_edited_by TEXT,
  date_modified TIMESTAMPTZ,
  comments JSONB DEFAULT '[]'::jsonb
);
License
MIT