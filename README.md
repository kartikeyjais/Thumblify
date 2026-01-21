🚀 Built a Full-Stack AI Thumbnail Generator (MERN + Google Gemini API)
I recently built a full-stack project called Thumblify — an AI Thumbnail Generator that helps creators instantly generate professional video thumbnails using AI.
Users can simply enter a video title, choose a style, aspect ratio, and color scheme, and the app generates a YouTube-style thumbnail with a live preview experience.

✅ Project Overview:
Thumblify is designed for content creators who want fast, high-quality thumbnails without manual designing. The thumbnails look bold, clean, and click-worthy — similar to YouTube creator thumbnails.

🎨 Frontend (React):
Built using React
A dedicated Thumbnail Preview Panel
User inputs:
Title/Topic
Aspect Ratio (16:9, etc.)
Styles (Bold, Futuristic, Minimalist...)
Color Schemes
Clean UI similar to YouTube thumbnail creation layout

⚙️ Backend (Node.js + Express):
Backend handles:
Prompt building logic
AI generation request
Thumbnail processing and saving
Created API routes for:
Generate Thumbnail
Fetch Thumbnail
Delete Thumbnail

🗄️ Database (MongoDB):
Stores thumbnail data like:
title
style
color scheme
aspect ratio
generated image URL
Helps users manage all generations inside the app

🔐 User Authentication:
Implemented user authentication to make it creator-friendly:
Register / Login / Logout
Session-based authentication
Each user can view only their own thumbnails

☁️ Image Hosting (Cloudinary):
Once thumbnail is generated:
it is uploaded to Cloudinary
stored as a secure image URL
then shown in preview + downloadable format

🤖 AI Integration (Google Gemini API)
Used Google Gemini API (Gemini model) to:
generate professional thumbnails from prompts
apply styles + colors + aspect ratio based on user selection
create visually stunning output designed for high CTR

🔁 CRUD Features (Creator Dashboard):
Users can:
✅ Generate thumbnails
✅ Preview thumbnails
✅ Download thumbnails
✅ Delete thumbnails
✅ Manage all designs in one place

🚀 Building an AI Thumbnail Generator — Key Challenge I Faced:

✅ 1) Session/Cookie Authentication issue in Production (Vercel)
Even after successful login, the app was showing “You are not logged in” because browser cookies were not being stored/sent properly across frontend + backend domains, requiring correct CORS + credentials + secure SameSite cookie configuration.

✅ 2) Frontend–Backend API payload mismatch:
Some features didn’t work initially because of wrong request key names / spelling mismatches between frontend and backend (example: aspect_ratio vs aspec_ratio, text_overlay vs text_overlays), causing the AI generation flow to break.


