# 🎨 AI Image Info Pro

A self-contained HTML application for managing AI-generated images and organizing the metadata, prompts, and settings used to create them.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![No Dependencies](https://img.shields.io/badge/dependencies-none-green.svg)
![Offline](https://img.shields.io/badge/works-offline-brightgreen.svg)

## ✨ Features

- **Local File Storage** - Preset data saved as JSON files alongside your images (survives browser cache clears!)
- **Folder Management** - Save multiple image folders and switch between them instantly
- **Image Processing** - Catalog your AI images with full metadata including prompts, models, LoRAs, and generation settings
- **Preset Library** - Build a searchable collection of your processed presets
- **Auto-Load Presets** - Existing preset files are automatically detected when loading a folder
- **Metadata Tracking** - Store positive/negative prompts, checkpoint models, LoRA configurations with strengths, CFG scale, steps, sampler, seed, and custom notes
- **Export Gallery** - Generate standalone HTML galleries of your preset collections
- **100% Local** - All data stays on your computer, no servers or cloud
- **No Installation** - Single HTML file, no server or dependencies required

## 🚀 Quick Start

1. **Download** the `aiimageinfoprov2.html` file
2. **Open** it in your web browser (Chrome/Edge recommended)
3. **Click** "Manage Folders" to add your first image folder
4. **Browse** to select a folder containing AI-generated images
5. **Click** the folder button to load images
6. **Select** images and click "Process Selected" to add metadata

## 📖 How to Use

### Adding Folders

1. Click the **"📂 Manage Folders"** button
2. Enter a friendly name for the folder (e.g., "Character Art", "Landscapes")
3. Click **"Browse"** and select the folder on your computer
4. Click **"Save"** to add it to your collection

### Loading Images

- Click any folder button in the **Active Folders** area
- Images will load and appear in the **"New Images"** tab
- Already-processed images are automatically filtered out

### Processing Images

1. Click images to select them (or use "Process All New")
2. Click **"Process Selected"**
3. Fill in the metadata form:
   - **Preset Name** - A memorable name for this preset
   - **Positive Prompt** - The prompt used to generate the image
   - **Negative Prompt** - Negative prompts used
   - **Checkpoint/Model** - The model file used (e.g., `realvisxlV40.safetensors`)
   - **LoRAs** - Add multiple LoRAs with their strength values
   - **CFG Scale** - Classifier-free guidance scale
   - **Steps** - Number of sampling steps
   - **Sampler** - Sampling method used
   - **Seed** - Generation seed (optional)
   - **Notes** - Any additional notes
4. Click **"Save Preset"**

### Viewing Presets

- Switch to the **"Processed Presets"** tab
- Click any preset card to view full details
- Use the **Copy** buttons to copy prompts and settings
- Click **"Edit"** to modify metadata or **"Download"** to export files

### Exporting

- Click **"Export Gallery"** to generate a standalone HTML file with all your presets
- The exported gallery can be opened in any browser and shared

## 🌐 Browser Compatibility

| Feature | Chrome/Edge | Firefox | Safari |
|---------|:-----------:|:-------:|:------:|
| Basic functionality | ✅ | ✅ | ✅ |
| File System Access API | ✅ | ❌ | ❌ |
| Instant folder switching (cached) | ✅ | ✅ | ✅ |
| Permission persistence | ⚡ Partial | ❌ | ❌ |

### Browser-Specific Behavior

#### Chrome / Edge (Recommended)
- Uses the **File System Access API** for better folder handling
- After closing and reopening, you'll see a quick permission prompt when clicking a folder button
- You don't need to navigate through folders again - just click "Allow"
- Within a session, switching between folders is instant

#### Firefox
- Falls back to standard file input for folder selection
- After closing and reopening, you must browse to select folders again
- Once loaded in a session, switching between cached folders is **instant**
- Look for the ⚡ indicator on folder buttons - these switch instantly

#### Safari
- Basic functionality works but not extensively tested
- Similar behavior to Firefox

## 💾 Data Storage

### Local File Storage (New!)

When you process an image, the app saves files directly to your image folder:

- `imagename_preset.json` - All metadata (prompts, model, LoRAs, settings)
- `imagename_thumb.jpg` - Thumbnail image

**This means:**
- ✅ Clear browser cache? No problem - just re-add the folder and presets reload automatically
- ✅ Move images to another computer? The preset data travels with them
- ✅ Back up your image folder? Presets are included
- ✅ Share a folder? Recipients get your presets too

### Browser Storage (Supplementary)

The app also uses browser storage for folder configurations:

- **localStorage** - Folder names and settings
- **IndexedDB** - Directory handles for Chrome/Edge persistent access

### Browser Differences

| Feature | Chrome/Edge | Firefox |
|---------|:-----------:|:-------:|
| Auto-save to folder | ✅ Automatic | ⬇️ Downloads for manual save |
| Read existing presets | ✅ | ✅ |

**Chrome/Edge:** Files are written directly to your image folder - completely automatic.

**Firefox:** When you save a preset, the JSON and thumbnail files download. You need to manually move them to your image folder. When loading, Firefox reads these files normally.

### Clearing Data

Click **"Clear All Data"** to remove browser-stored folder configurations. **Your preset files in the image folders are NOT deleted** - they stay safe with your images.

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Esc` | Close any open modal |
| `Ctrl + Enter` | Save preset (when in form) |
| `E` | Edit preset (when viewing) |

## 📁 File Structure

```
aiimageinfoprov2.html    # The entire application (single file)
```

That's it! Everything is contained in one HTML file including all CSS and JavaScript.

## 🔧 Technical Details

- **No build process** - Pure HTML/CSS/JavaScript
- **No dependencies** - No external libraries required
- **No server needed** - Works with `file://` protocol
- **Responsive design** - Works on desktop and tablet screens
- **Dark theme** - Easy on the eyes for extended use

## 📝 Tips

1. **Use Chrome/Edge for best experience** - Automatic file saving to your folders
2. **Firefox users** - When prompted, save downloaded files to the same folder as your images
3. **Organize by project** - Create separate folders for different art projects
4. **Regular backups** - Your image folders now contain all preset data - back them up!
5. **Moving computers** - Just copy your image folder - presets come with it

## 🐛 Known Limitations

- Firefox requires manual file saving (downloads files instead of writing directly)
- Very large folders (1000+ images) may take a moment to load
- Browser security requires re-authorization after closing (but your preset files remain safe in the folder)

## 📄 License

MIT License - Feel free to use, modify, and distribute.

---

Made for AI artists who want to keep their creative work organized. 🎨
