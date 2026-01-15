# Together BCIT — BBY15 Team Project

## Overview

**Together BCIT** is a mobile-friendly web application designed to support **new BCIT students**, especially international and out-of-province students, as they settle into life in Vancouver.

Live: https://bby15-comp1800.web.app

The app helps students:

- explore important locations on an interactive Mapbox map
- read and create discussion posts related to those places
- customize a personal profile and share helpful information
- connect with other BCIT students through forums

Our goal is to make it easier for newcomers to feel supported, informed, and connected.

---

## Features

### 🗺️ Interactive Map

- Custom Mapbox markers for essential locations (banks, groceries, transit, pharmacies, government offices, etc.).
- Popups with location details and quick links to related forum posts.
- Distance from user shown for each location.
- Mobile-friendly layout with collapsible filters.
<p align="center" width="100%">
  <img src="images/map-preview.jpg" alt="Map Preview Image" text-align="center" width="50%"/>
</p>

### 💬 Forum System

- Browse all posts or filter by category.
- Create posts and attach images.
- Create posts tied to a map location.
- View full threads with nested comments.
- Delete option for post owners.
<p align="center" width="100%">
  <img src="images/how-step-3.png" alt="Forum Preview Image" width="50%"/>
</p>

### 👤 Profile Page

- Upload/change profile picture.
- Display personal information from Firestore.
- View your posts.
- Logout and account state handled through Firebase Auth.
<p align="center" width="100%">
  <img src="images/profile-preview.png" alt="Profile Preview" width="50%"/>
</p>

---

## Technologies Used

### Frontend

- HTML5, CSS3, JavaScript
- Web Components
- Responsive design with custom CSS
- Mapbox GL JS

### Backend / Cloud

- **Firebase Authentication** (user login/signup)
- **Firestore Database** (threads, comments, users, locations)
- **Firebase Hosting**
- **Firebase Storage** (profile images & post images)

### Development Tools

- **Vite** for local dev server and building
- **Git & GitHub** for version control
- **Canva/Figma** for design assets
- VS Code

---

## Usage

1. Open the landing page (`index.html`).
2. Explore the **interactive map** and click markers to see categories and related posts.
3. Use filters or search the map to find specific places.
4. Visit the **forum** to browse, search, or filter posts.
5. Create a new post (with optional image compression).
6. If logged in, edit your **profile** and upload a profile picture.
7. Log out through the profile page.

---

## Project Structure

```
1800_202530_BBY15/
├── index.html
├── loginPage.html
├── map.html
├── forumMain.html
├── forumnew.html
├── forumpost.html
├── editProfile.html
├── profilePage.html
├── secret.html
├── Skeleton.html
├── 404.html
│
├── src/
│   ├── authentication.js              # Login/Signup backend logic (Firebase Auth)
│   ├── editProfile.js                 # Profile editing (bio, name, photo updates)
│   ├── firebaseConfig.js              # Firebase initialization + service exports
│   ├── forum-main.js                 # Forum homepage: list posts, filters, location context
│   ├── forumnew.js                   # Page to create a new post (with image compression)
│   ├── forumpost.js                  # Single post page + comments + like/dislike
│   ├── loginSignup.js                # UI logic for login/signup page
│   ├── main.js                       # Landing page helper logic
│   ├── map.js                        # Interactive Mapbox map + filters + distance + popups
│   ├── navBar.js                     # (Deprecated) older navbar version
│   ├── profile.js                    # Loads and displays user profile data
│   ├── scrollReveal.js               # Scroll animation effects used on landing page
│   ├── secret.js                     # Easter-egg “secret page” logic
│   └── components/
│       └── default-components.js     # Web components: navbar + footer
│
├── styles/
│   ├── forum-style.css               # Forum pages styling
│   ├── loginPage.css                 # Login / signup styling
│   ├── map-styles.css                # Styles for Mapbox page (map responsivity, filters)
│   ├── profile-page.css              # Styles for profile page + profile editing
│   ├── secret.css                    # Style for secret easter-egg page
│   └── style.css                     # Global theme: colors, fonts, footer, navbar, layout
│
├── images/
│   ├── defaultProfilePicture.png
│   ├── dislikeButton.png
│   ├── forum.png
│   ├── forum-preview.png
│   ├── how-step-1.png
│   ├── how-step-2.png
│   ├── how-step-3.png
│   ├── istockphoto-1453719077-612x612.jpg
│   ├── likeButton.png
│   ├── logoImg.png
│   ├── map-preview.jpg
│   ├── maps.png
│   ├── profile.png
│   ├── profile-preview.png
│   ├── secret.png
│   └── icons/
│       ├── bank.png
│       ├── default.png
│       ├── education.png
│       ├── goverment.png
│       ├── groceries.png
│       ├── pharmacy.png
│       └── shopping.png
│
├── .env
├── .gitignore
├── cors.json
├── firebase.json
├── firestore.rules
├── firestore.indexes.json
├── storage.rules
├── package.json
├── package-lock.json
├── vite.config.js
└── README.md

```

---

## Contributors

- **Tyson** — Firebase logic, map integration, debugging.
- **Maria Fernanda** — UI/UX, front-end logic, Firestore locations, documentation.
- **Thor** — Forum system, comment handling, backend logic.
- **BBY15 Team** — Collaborative group that supports each other and learns quickly.

---

## Acknowledgments

### Images & Icons

- Icons sourced from **Flaticon**, **Icons8**, **Canva**, and free-use icon packs.
- Landing images used under educational fair use.
- User-uploaded images stored in Firebase Storage.

### Libraries & APIs

- Mapbox GL JS
- Firebase (Auth, Firestore, Storage, Hosting)
- Vite
- Bootstrap (limited use)

### Code References

Snippets adapted from:

- BCIT COMP1800 course materials
- Mapbox documentation
- Firebase documentation
- Helpful examples from StackOverflow

All code was adapted and rewritten for this project.

---

## Limitations and Future Work

### Current Limitations

- Comments cannot include images.
- Location list must be manually updated.
- No admin/moderation features.
- Mapbox default POIs cannot be removed or integrated with custom posts.

### Future Improvements

- Add messaging or friend system.
- Auto-generate categories/tags from Mapbox.
- Expand profile customization.
- Recommendation engine for locations or posts.
- Dark mode theme.

---

## License

This project is for educational purposes (BCIT COMP 1800).  
External libraries follow their respective licenses (MIT, Mapbox, Firebase).
