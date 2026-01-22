# Horika Gallery

A photo gallery showcasing images captured with the [Horika app](https://omitlens.com/apps/horika) — a film simulation camera app that celebrates the randomness and imperfect beauty of analog photography.

## 📁 Structure

```
gallery/
├── index.html          # Gallery page with lightbox functionality
├── script.js           # Gallery logic and lightbox interactions
├── style.css           # Gallery styles
├── images.json         # Image metadata and photographer attribution
├── horikan.json        # Photographer profile information
├── images/             # Gallery image files (AVIF format)
└── README.md          # This file
```

## 🖼️ How It Works

The gallery dynamically loads images from JSON configuration files:

- **`images.json`** - Contains an array of image objects with filenames and photographer attributions
- **`horikan.json`** - Contains photographer profile information (name, bio, link)
- **`script.js`** - Loads the JSON files, renders the gallery grid, and handles the lightbox overlay

### Featured Image

A random image is selected and displayed as the featured hero image on page load. Clicking it opens a lightbox view.

### Gallery Grid

All images from `images.json` are displayed in a masonry-style grid. Each image can be clicked to view in a full-screen lightbox with photographer attribution.

## ➕ Adding New Images

### Step 1: Add Image Files

1. Convert your images to AVIF format for optimal performance:

   ```bash
   # Using ImageMagick
   mogrify -format avif IMAGE.jpeg
   ```

2. Copy the AVIF files to the `images/` folder
3. Use a consistent naming convention (e.g., `IMG_XXXX.avif`)

### Step 2: Update `images.json`

Add new entries to the images array in `images.json`:

```json
{
  "file": "IMG_8616.avif",
  "horikan": "Jun Lin"
}
```

**Fields:**

- `file` (string, required): The filename in the `images/` folder
- `horikan` (string, required): The photographer's name (must match a name in `horikan.json`)

**Example:**

```json
[
  {
    "file": "IMG_7216.avif",
    "horikan": "Jun Lin"
  },
  {
    "file": "IMG_7241.avif",
    "horikan": "Jun Lin"
  },
  {
    "file": "YOUR_NEW_IMAGE.avif",
    "horikan": "Your Name"
  }
]
```

### Step 3: Update Photographer Profile (if needed)

If adding photos from a new photographer, update `horikan.json`:

```json
{
  "name": "Your Name",
  "bio": "Brief bio or description",
  "link": "https://yourwebsite.com"
}
```

**Fields:**

- `name` (string, required): Photographer's display name
- `bio` (string, optional): Short biography or description
- `link` (string, optional): URL to photographer's website or portfolio

**Note:** Currently, `horikan.json` supports a single photographer profile. For multiple photographers, the structure may need to be updated to an array format.

## 🎨 Image Requirements

- **Format:** AVIF (preferred for performance)
- **Orientation:** Both portrait and landscape supported
- **Size:** Recommended maximum 2000px on longest edge
- **File naming:** Use consistent naming (e.g., `IMG_XXXX.avif`)

## 📝 JSON Schema

### images.json

```json
[
  {
    "file": "string (required)",
    "horikan": "string (required - photographer name)"
  }
]
```

### horikan.json

```json
{
  "name": "string (required)",
  "bio": "string (optional)",
  "link": "string (optional - URL)"
}
```

## 🎯 Features

- **Random Featured Image**: Each page load displays a different featured image
- **Lightbox View**: Click any image for full-screen viewing
- **Responsive Grid**: Masonry-style layout adapts to different screen sizes
- **Photographer Attribution**: Each image displays photographer info in the lightbox
- **Photo Submission**: UI includes a "Submit your photo" button for community contributions
